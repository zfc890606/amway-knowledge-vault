---
name: douyin-video-fetcher
description: >
  MUST USE when user shares a douyin/TikTok video link and needs to extract
  the video description/text content. 当用户发抖音链接需要提取视频文案时使用。

  原理：利用 iesdouyin.com 的 SSR 页面提取 window._ROUTER_DATA 中的完整视频信息。
  不需要 Cookie/登录态，完全免费。

  NOT for: 提取语音转写字幕（只能获取视频简介文字，不是语音识别）
triggers:
  - 抖音: douyin/抖音/抖音链接/抖音视频/v.douyin.com/iesdouyin
metadata:
  source: https://iesdouyin.com
  type: content-extractor
---

# 🎬 抖音视频文案提取器 — douyin-video-fetcher

> **一句话本质**：利用 iesdouyin.com 的 SSR（服务端渲染）页面，提取 `window._ROUTER_DATA` 中的完整视频信息，无需登录、无需 Cookie、完全免费。

---

## 原理

抖音官方页面（`v.douyin.com`）有反爬限制，直接在浏览器或 curl 请求拿不到完整信息。

**iesdouyin.com** 是一个第三方镜像站，它的 SSR 页面在 HTML 中直接注入了 `window._ROUTER_DATA`，包含视频的所有元信息——标题、描述、作者、统计数据等。

只需要用 Python requests 请求 `https://iesdouyin.com/video/{video_id}`，然后用正则提取 `window._ROUTER_DATA` 中的 JSON 即可。

---

## 使用方法

### 第一步：从抖音链接提取 video_id

抖音链接格式：
```
https://v.douyin.com/XXXXXXX/
```
1. 用浏览器打开这个链接（或在 Obsidian 中直接打开）
2. 它可能会跳转到 `douyin.com/video/{video_id}` 格式
3. 从跳转后的 URL 中提取 `video_id`（通常是一串数字）

或者直接观察链接中的 `/video/` 后面那串数字就是 video_id。

### 第二步：运行 Python 脚本

```python
import re
import json
import requests

def fetch_douyin_video(video_id: str) -> dict:
    """
    从 iesdouyin.com 获取抖音视频信息

    Args:
        video_id: 抖音视频 ID（纯数字，或带斜杠的完整路径）

    Returns:
        包含视频信息的字典，关键字段见下方说明
    """
    url = f"https://iesdouyin.com/video/{video_id}"
    headers = {
        "User-Agent": (
            "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) "
            "AppleWebKit/537.36 (KHTML, like Gecko) "
            "Chrome/120.0.0.0 Safari/537.36"
        ),
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8",
        "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8",
    }

    resp = requests.get(url, headers=headers, timeout=15)
    resp.raise_for_status()

    # 提取 window._ROUTER_DATA
    pattern = r'<script>window\._ROUTER_DATA\s*=\s*({.*?})</script>'
    match = re.search(pattern, resp.text, re.DOTALL)
    if not match:
        raise ValueError("未找到 _ROUTER_DATA，页面结构可能已变化")

    data = json.loads(match.group(1))
    return data


def parse_video_info(raw: dict) -> dict:
    """
    从 _ROUTER_DATA 中提取关键信息

    Args:
        raw: _ROUTER_DATA 解析后的字典

    Returns:
        结构化的视频信息
    """
    try:
        # 路由结构通常为 loaderData -> video/(id) -> videoInfo -> ...
        loader = raw.get("loaderData", {})
        # 找到 video route
        video_route = None
        for key, val in loader.items():
            if key.startswith("video/"):
                video_route = val
                break

        if not video_route:
            raise ValueError("找不到 video route")

        video_info = video_route.get("videoInfo", {}).get("video", {})
        author_info = video_route.get("authorInfo", {})
        statistics = video_info.get("statistics", {})

        return {
            "desc": video_info.get("desc", ""),           # 视频文案/描述
            "author": author_info.get("nickname", ""),     # 作者昵称
            "author_id": author_info.get("uniqueId", ""),  # 作者抖音号
            "author_avatar": author_info.get("avatarThumb", ""),
            "cover": video_info.get("cover", ""),          # 封面图 URL
            "duration": video_info.get("duration", 0),     # 时长（秒）
            "play_count": statistics.get("playCount", 0),
            "like_count": statistics.get("diggCount", 0),
            "comment_count": statistics.get("commentCount", 0),
            "share_count": statistics.get("shareCount", 0),
            "create_time": video_info.get("createTime", ""),
            "music_title": video_info.get("music", {}).get("title", ""),
        }
    except (KeyError, TypeError) as e:
        raise ValueError(f"解析视频信息失败: {e}")


# ═══════════════════════════════════════════════════
# 使用示例
# ═══════════════════════════════════════════════════

if __name__ == "__main__":
    # 替换为你要提取的视频 ID
    video_id = "7372685392518122791"

    raw = fetch_douyin_video(video_id)
    info = parse_video_info(raw)

    print("=" * 50)
    print(f"📝 文案内容：")
    print(info["desc"])
    print()
    print(f"👤 作者：{info['author']} (@{info['author_id']})")
    print(f"▶️ 播放：{info['play_count']}  👍 点赞：{info['like_count']}")
    print(f"💬 评论：{info['comment_count']}  🔄 分享：{info['share_count']}")
    print(f"🎵 音乐：{info['music_title']}")
    print("=" * 50)
```

### 输出示例

```json
{
  "desc": "所有人必须用AI，不用的踢出去...",
  "author": "姜胡说",
  "author_id": "JiangHuShuo",
  "play_count": 235000,
  "like_count": 15200,
  "comment_count": 876,
  "share_count": 2340
}
```

---

## 字段说明

| 字段 | 类型 | 说明 |
|------|------|------|
| `desc` | string | **视频文案/描述** —— 这就是我们需要的口播文案（注意：不是语音转写，是作者写在简介里的文字） |
| `author` | string | 作者昵称 |
| `author_id` | string | 作者抖音号（uniqueId） |
| `duration` | int | 视频时长（秒） |
| `play_count` | int | 播放量 |
| `like_count` | int | 点赞数 |
| `comment_count` | int | 评论数 |
| `share_count` | int | 分享数 |
| `create_time` | string | 发布时间 |
| `music_title` | string | 背景音乐标题 |

---

## ⚠️ 注意事项

### 能拿什么
- ✅ 视频简介/描述文字（desc 字段）—— 大部分创作者的完整口播文案会放在这里
- ✅ 作者信息、统计数据（播放/点赞/评论/分享）
- ✅ 封面图、背景音乐信息

### 不能拿什么
- ❌ **语音转写字幕** —— 如果作者没有把文案写在 desc 里，这个方案拿不到口播内容（需要语音识别）
- ❌ 评论内容（只能拿到评论数）
- ❌ 视频下载（只能拿封面，不能拿视频文件）
- ❌ 需要登录态的私密/付费内容

### 容错处理

如果脚本返回 `ValueError: 未找到 _ROUTER_DATA`，可能原因：
1. **video_id 格式不对** —— 确认是纯数字 ID，不是完整 URL
2. **iesdouyin.com 被屏蔽** —— 换网络环境（手机热点 -> Wi-Fi）
3. **页面结构变更** —— 打开 `https://iesdouyin.com/video/{id}` 在浏览器中查看 HTML，检查 `_ROUTER_DATA` 是否还在

### 使用限制

- 本工具仅用于提取**公开可见**的抖音视频信息，遵守相关法律法规
- 不要高频请求，建议两次请求间隔至少 2 秒
- 单个 IP 的请求频率过高可能被限流

---

## 🔗 关联

- 所属分类：[[知识库/05-Skills（技能sop）/短视频方法库/内容获取类|内容获取类]] 
- 同分类参考：[[知识库/05-Skills（技能sop）/短视频方法库/内容获取类/视频号内容获取]]
- 流水线上下文：[[知识库/00-操作系统总控台]] → 输入来源标注 "抖音链接自动走 douyin-video-fetcher 提取文案"
- 对应问题：[[知识库/00-灵感库（标记灵感）/问题排行榜]] #1 "想太多不行动"
- 关联卡片：[[知识库/00-灵感库（标记灵感）/知识卡片/KC-创业-014-换系统思维：铁锹变拖拉机，靠系统不靠意志力]]

---

> v1.0 · 2026-07-16 · 基于 iesdouyin.com SSR 方案
