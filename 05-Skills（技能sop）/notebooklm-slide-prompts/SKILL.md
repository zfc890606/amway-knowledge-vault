---
name: notebooklm-slide-prompts
description: NotebookLM/Kael.im 幻灯片设计提示词库 — 精选自 X/Twitter、小红书、Note 等平台的 20+ 种幻灯片视觉风格提示词，覆盖 editorial、pop、艺术、专业、运动等风格谱系。
version: 1.0.0
metadata:
  source: https://github.com/serenakeyitan/awesome-notebookLM-prompts
  license: CC BY 4.0
---

# NotebookLM 幻灯片设计提示词库

> 精选自全球创作者社区的 NotebookLM & Kael.im 幻灯片设计提示词，涵盖 editorial、pop、艺术、专业、运动等风格谱系。

## 使用方式

将对应风格的提示词（代码块内容）直接复制到 NotebookLM 或 Kael.im 的提示词输入框中，配合你的内容素材生成幻灯片。

**关键指令**：如果需要提示词使用中文输出，在提示词中注明 `the language should be what users said in the prompt`（或替换为你需要的语言）。

---

## 📂 风格目录

### A. Editorial & Business 编辑商业风
- [Modern Newspaper 现代报刊](#modern-newspaper)
- [Sharp-edged Minimalism 锐利极简](#sharp-edged-minimalism)
- [Yellow × Black Editorial 黄黑编辑风](#yellow-x-black-editorial)
- [Black × Orange Creative Agency 黑橙创意社](#black-x-orange-creative-agency)
- [Seminar Use 研讨极简](#seminar-use)

### B. Pop, Youth & Street 流行街头风
- [Manga Style 漫画风](#manga-style)
- [Magazine Style 杂志风](#magazine-style)
- [Pink Street-style 粉红街头](#pink-street-style)
- [Digital / Neo Pop 数字新流行](#digital-neo-pop)

### C. Typography 字体驱动风
- [Mincho × Handwritten Mix 明朝体手写混搭](#mincho-x-handwritten-mix)

### D. Artistic & Avant-Garde 艺术前卫风
- [Deformed Flat Persona 变形扁平人设](#deformed-flat-persona)
- [Royal Blue × Red Watercolor 蓝红水彩](#royal-blue-x-red-watercolor)
- [Classic / Pop 古典波普](#classic-pop)
- [Tech / Art / Neon 科技艺术霓虹](#tech-art-neon)

### E. Professional / Premium 专业高级风
- [Studio / Mockup / Premium 工作室高保真](#studio-mockup-premium)

### F. Sports & High-energy 运动能量风
- [Sports / Athletic / Energy](#sports-athletic-energy)

### G. Conceptual 概念风
- [Anti-Gravity / Artifact Deck 反重力器物](#anti-gravity-artifact-deck)

---

## Modern Newspaper

**风格**：洗练商业媒体 · 瑞士风格/包豪斯灵感 · 非对称布局 · 超大标题占比30-50%

![Preview](https://hackmd.io/_uploads/SkkpwiPM-g.png)
![Preview](https://hackmd.io/_uploads/rJZ0pyKGbg.png)
![Preview](https://hackmd.io/_uploads/Hya0p1FzZx.png)

````
You are a top art director leading Japan's "new economy business media." But the language should be what users said in the prompt. so not nessecery in (the language what users requested in the prompt).
Based on the following "design definition," generate a visually focused, high-sensibility presentation slide that sparks intellectual excitement in business professionals of the smartphone generation.

[Important: Absolutely Prohibited Output Format Rules]
* **Complete Exclusion of Markdown Symbols**: Do not include symbols like "#" for headings or "*" and "**" for emphasis in the slide text **under any circumstances**.
* **Plain Text Only**: Text displayed on the slide must consist solely of "pure (the language what users requested in the prompt) and English text" without any decorative symbols.

[Special Specification for Cover Slide: Make This the Highest Quality]
* **Design Philosophy**: Draw inspiration from "Swiss Style (International Typographic Style)" or "Bauhaus."
* **Layout**: Ban simplistic "centered alignment." Create tension with **"asymmetrical"** placement. Use a grid system to position the title extremely off to the top left or bottom left, or craft bold negative space for refinement.
* **Title Copy Design**:
    * **Main Title (Ultra-Large · Short Phrase)**: Ditch descriptive words. Make it a visual anchor with a short word or phrase of about "2–5 characters" (e.g., "Liberation," "Collapse and Rebirth," "The True Face of AI").
    * **Subtitle (Ultra-Small · Benefit-Driven)**: Carve into the reader's pain points and hint at resolution with a concise sentence (e.g., "Why Is Your Advertising Dead?" "How to Ditch 'Tasks' and Return to 'Creation'").
    * **Composition Ratio**: Punch the eyes with the main title, stab the brain with the subtitle.

[Overall Design Definition for All Slides]
1.  **Core Theme**: Smart & pop business infotainment (intellectual curiosity × entertainment)
2.  **Color Palette**:
    * Background Color: White (#FFFFFF) or Cool Gray (#F5F5F5)
    * Text Color: Sumi (Jet Black) (#111111)
    * Accent Color: Electric Yellow (#FFCC00) or Alert Red (#FF3333)
3.  **Visual Style**:
    * Adopt the design philosophy of a "**smartphone-first economic media**."
    * Use images like "monochrome cutouts of people" or "stylish photos with blown-out backgrounds" to emphasize the subject.
    * Highlight key numbers or keywords with fluorescent marker-style lines (yellow background) to create rhythm.

4.  **Typography (Text as Graphic)**:
    * Position headlines at an "**ultra-massive size**" occupying **30%–50%** of the slide's area.
    * **Extreme Jump Ratio**: The size ratio between "headlines" and "body text" must be **10:1** or more. No half-hearted size differences allowed.
    * For headlines, use **extra-bold sans-serif** (Impact/(Hiragino) W8 weight) to treat them as a "surface," and tuck ultra-thin English fonts into the gaps for a sense of airiness.

5.  **Overall Structure**:
    * Strictly adhere to "1 slide = 1 message."
    * Layout is a binary choice between "negative space" or "text." Draw the eye through contrasts of text-packed areas that fill the screen and vast empty voids.
    * Place the conclusion (punchline) with a "bam!" in the center of the slide, or position it spilling off the edge for visual impact.
````
*来源：https://x.com/mmmiyama_D/status/1998528702150488069*

---

## Sharp-edged Minimalism

**风格**：锐利极简·建筑感·左上角导航·网格系统

![Preview](https://hackmd.io/_uploads/S1AgdjvzZx.png)
![Preview](https://hackmd.io/_uploads/r16fOsDMZe.png)

````
# presentation_design_spec_minimal_jp.yaml
# Style: Refined Minimal Portfolio
# Characteristics: Top-left navigation, aesthetics of whitespace, grid-based layout

Global Design Settings:
  Tone: "Professional, architectural, sharp-edged minimalism"
  Color Palette:
    Base: "#E9E9E9 (light gray) or #FFFFFF (white)"
    Text: "#000000 (jet black) or #333333 (dark gray)"
    Accent: "#000000 (black) – used for bold lines and emphasized text"
    Special: "Dark mode (black background) – used for slides that need emphasis"
  Typography:
    Headings: "English sans-serif (e.g., Helvetica Now, Inter). Bold and decoratively positioned."
    Body: "(the language what users said in the prompt) Gothic typeface. Small size with generous letter spacing and line height." But the language should be what users said in the prompt.
  Common Layout Rules:
    Navigation: "Place a small section number and title such as '01. INTRODUCTION' in the top-left (or top-right) of every slide."
    Grid: "Use a strict grid system to align elements."
    Whitespace: "Intentionally leave large areas empty (negative space) to create a sense of luxury."

Layout Variations:
  - Type: "Title Typography" — Scattered layout. Randomly place award badges or keywords like stamps.
  - Type: "Text + Data Emphasis" — Asymmetrical split. Narrative text on left, oversized numbers on right.
  - Type: "Card Grid" — Tightly spaced grid of high-quality images.
  - Type: "Full-Screen Graphic" — Office interior photography, reduce saturation for cool tone.
  - Type: "Photo + List Split" — 50:50 split, architectural photo on left, data list on right.
  - Type: "Minimal Map" — Silhouette-style map with ultra-thin callout lines.
  - Type: "Vertical Timeline" — Single thin vertical line with text branching left and right.
  - Type: "Bubble Chart / Venn Diagram" — Wireframe style, black background with thin white line art.
  - Type: "Dialogue (Chat Style)" — Simple text blocks with bold speaker names.
  - Type: "Chronological List" — Large years on left, descriptions on right.
  - Type: "Dark Mode Diagram" — Black background with thin white lines connecting nodes.
  - Type: "3-Step Columns" — Large numbers (01, 02, 03) as pillars.
  - Type: "Logo Grid" — Monochrome grid of logos in strict alignment.
  - Type: "Two Columns (Problem vs Solution)" — Thick black vertical line separating columns.
  - Type: "Centered Layout (Dark Mode)" — Cinematic centered visual on black background.
  - Type: "Formula / Flow Diagram" — Mathematical style, large serif type.
  - Type: "Arrow Steps" — Linear process with text inside large arrows.
  - Type: "Chart" — Thin lines with small black dots, scientific instrument appearance.
````
*来源：https://x.com/yoshifujidesign/status/1997878247322001626*

---

## Yellow × Black Editorial

**风格**：黄底黑字·大号现代衬线字体·时尚摄影·波普手绘贴纸

![Preview](https://hackmd.io/_uploads/r1CQYiwz-l.jpg)
![Preview](https://hackmd.io/_uploads/SymEYsDM-g.jpg)

```
Yellow background, black text, large dynamic modern serif font placement, stylish, photos are unique fashion photography, with pop and chic touches like handwriting or stickers scattered throughout, bold layout like a fashion magazine
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Black × Orange Creative Agency

**风格**：白底黑字+血橙色点缀·创意社风格

![Preview](https://hackmd.io/_uploads/rJtz5yFMWx.png)
![Preview](https://hackmd.io/_uploads/ryZ0YJtfWe.png)

```
Background is white, text is black, accent color is blood orange, stylish design that a creative agency might create, incorporating dynamic and simple photos and English typography. But the language should be what users said in the prompt.
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Seminar Use (Minimal Text)

**风格**：极简文字·白底黑字红点缀

![Preview](https://hackmd.io/_uploads/HJASpkYGbl.png)
![Preview](https://hackmd.io/_uploads/Bks861tGWx.png)

```
White background, black text, red accent color, sans-serif font, high-quality photo like a fashion portrait, dynamic typography, high-sensibility design
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Manga Style

**风格**：漫画风·用故事+漫画提高理解度

![Preview](https://hackmd.io/_uploads/SygJvqkKf-l.png)
![Preview](https://hackmd.io/_uploads/r1Ew9yYMZl.png)

```
Understanding becomes deeper with "fun." Sometimes, it's recommended to turn information into a comic and input it along with a story. You can relate it to your own situation, and it's easier to remember.
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Magazine Style

**风格**：成熟可爱杂志风·剪影照片·手绘气泡

![Preview](https://hackmd.io/_uploads/rkQpqyKfbg.png)

```
# Instructions
Please compile [Source Information] in a [mature-cute, sophisticated magazine-style editorial design].

# Layout Requirements
・Place a large cutout photo of the subject (model woman or product) in the center, emphasizing movement or pose
・Place speech bubbles or text boxes asymmetrically in the left and right margins
・Distribute main points as small sections numbered like "NO.1" "NO.2"
・Place a vertical text box (white background) at the edge of the screen (e.g., right side) and insert a catchy copy
・Place L-shaped lines resembling crop marks ("trim marks") in the four corners to create a poster or page-like feel
・Format: Landscape (4:3 or 3:2), high resolution
・But the language should be what users said in the prompt.

# Design Requirements
・Background color: Matte, subdued tone stylish pink (dusty pink or shell pink)
・Main image: Use a photo with the background completely removed (deep etching)
・Decorative elements: Use hand-drawn style speech bubbles, simple circles, and thin straight lines as accents
・Fonts: Headings in sophisticated Gothic or Mincho, comments in hand-drawn style font for a casual feel
・In speech bubbles or text boxes, write key points from the source information in emotional handwritten text of a young woman
・Color palette: Matte pink for background, charcoal gray or black for text, white for accents
・Overall atmosphere: Mature-cute, feminine, trendy, polished tone

# Expressions to Avoid
・Overly childish vivid colors, overly flashy gradients, heavy shadows
```
*来源：https://x.com/tetumemo/status/1996930284500201685*

---

## Pink Street-style

**风格**：粉色背景·白黑文字·厚线条插画·街头波普

![Preview](https://hackmd.io/_uploads/SJJDi1KzZe.png)
![Preview](https://hackmd.io/_uploads/S1PsJKM-l.png)

```
Background is pink, text is white and black, illustrative illustrations are pop and deformed illustrations drawn with thick lines, overall street style but pop, flat colors, photos are trimmed into soft and squishy shapes to create a sense of looseness,
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Mincho × Handwritten Mix

**风格**：明朝体+手写混搭·黄底黑字·时尚杂志感

![Preview](https://hackmd.io/_uploads/RkcRhytMWg.png)
![Preview](https://hackmd.io/_uploads/r1D1a1Yfbe.png)

```
Yellow background, black text, large dynamic modern serif font placement, stylish, photos are unique fashion photography, with pop and chic touches like handwriting or stickers scattered throughout, bold layout like a fashion magazine
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Digital Neo Pop

**风格**：维生素波普·数字新潮·有机形状·SNS友好视觉

![Preview](https://hackmd.io/_uploads/HyXkPgFM-g.png)
![Preview](https://hackmd.io/_uploads/BJOywxYfbx.png)

````
# presentation_design_spec_pop_jp.yaml
# Style: Vitamin Pop / Digital Neo
# Characteristics: Organic shapes, bright color palette, SNS-friendly visual tone

Global Design Settings:
  Design Theme: "Digital Pop × Academic"
  Tone & Manner: "Modern, fluid, friendly, high information density"

  Key Visuals:
    Motifs: "Organic amoeba-like or cloud-like shapes. Random placement around slide edges, partially cropped."
    Decorations: "Dot patterns, hand-drawn highlight strokes, SNS-style icon decorations"

  Color Palette:
    Base: "White (#FFFFFF) or light-gray dot-pattern background"
    Main Colors: "Vivid pink, cyan, purple (neon-sign inspired)"
    Accent: "Black (used for text and outlines to anchor the pop colors)"
    Chart Colors: "Gradient-filled bars (e.g., green → yellow)"

  Typography:
    Headings: "Bold gothic type. Impact-focused. Outline text (white fill + black stroke) allowed."
    Body: "Highly readable gothic sans serif."
    Numbers: "Large Western type for emphasis, especially percentages."

Design Guidelines:
  - Organic Shapes: "Use irregular, hand-drawn, wavy shapes rather than strict rectangles or circles."
  - Icons: "Prefer pop illustrations or abstract avatar icons over photos of real people."
  - Information Contrast: "Balance text-heavy slides with highly visual slides."

Layout Variations:
  - Type: "Title Composition" — Organic blob/cloud shape at center with title inside. Small stars and sparkles.
  - Type: "Text + Data Pop" — Split layout: left = text, right = colorful donut chart.
  - Type: "Organic Timeline" — Wavy vertical line like a plant stem with leaf/bud icons.
  - Type: "Bubble Cluster" — Overlapping translucent circles like soap bubbles.
  - Type: "SNS Chat Style" — Smartphone-style frame containing chat bubbles.
  - Type: "Concept Formula / Flow Diagram" — Hand-drawn arrows, icons, crayon-like strokes.
  - Type: "Colorful Step Flow" — Large arrow flowing left → right, each step in different color.
  - Type: "Lollipop Chart" — Lollipop-style bars with round tips.
  - Type: "Sticker Grid" — Slightly tilted square cards, taped/stickered appearance.
  - Type: "Character Ending" — Cloud/amoeba character in center with SNS icons around.
````
*来源：https://note.com/yoshifujidesign/n/n7412bccb5762*

---

## Royal Blue × Red Watercolor

**风格**：皇家蓝与红·湿水彩质感

![Preview](https://hackmd.io/_uploads/H1gBCkKGbx.png)
![Preview](https://hackmd.io/_uploads/rJDuCkKzWl.png)
![Preview](https://hackmd.io/_uploads/H1yiCyFzZe.png)

```
Shades of royal Blue and Red wet watercolor. Focus on different artistic styles to be used with kael/notebooklm Slides decks.
```
*来源：https://x.com/kottley/status/1994442047579721782*

---

## Studio / Mockup / Premium

**风格**：高保真工作室·Apple产品3D模型·极简UI展示

![Preview](https://hackmd.io/_uploads/BkZwrxtzWl.png)
![Preview](https://hackmd.io/_uploads/SyYvrxYzWe.png)

````
# presentation_design_spec_premium_mockup_jp.yaml
# Style: Premium Mockup / Modern UI / Clean Tech
# Concept: "Showcase in Perfection"

Global Design Settings:
  Tone: "High-quality, advanced, clean, refined, professional"

Color Palette:
  Background:
    - "#FFFFFF (pure white)"
    - "#F5F5F7 (very light gray, studio-like)"
    - "#000000 (jet black, switching by slide)"
  Accent Colors:
    - "#8D59E9 (Electric Purple – main action color)"
    - "#EBE021 (Acid Yellow – highlight points & badges)"
  Sub Colors:
    - "#D8E2EC (pale blue-gray for cards and base areas)"
    - "#2D2D2D (charcoal for text and UI parts)"

Visual Identity:
  Devices: "High-quality 3D mockups of Apple products (Studio Display, MacBook Pro, iPad, iPhone)"
  UI Screen Design:
    Background: "Jet black (#000000) or vivid gradients (purple, yellow, orange)"
    Typography: "Extra-bold sans serif (e.g., Helvetica Now Display Bold) in white"
    Layout: "Card-based UI, grid layout, oversized numbers"

Layout Variations:
  - Type: "Hero Display" — Center Studio Display with black-background UI
  - Type: "Floating Mobile" — Float an iPhone mockup in mid-air with blurred accent lighting
  - Type: "Grid Interface" — Inside a MacBook screen, colorful UI cards in grid
  - Type: "Dark Mode Presentation" — Device screen in dark mode with high-contrast accents
  - Type: "Angle Shot" — Device from diagonal side angle
  - Type: "Split Screen" — Left: half device mockup; Right: large typography
  - Type: "Card Grid (Text Only)" — Extend device UI layout to whole slide
  - Type: "Big Typography" — Black background with massive white text
  - Type: "Split UI" — Left: large numbers; Right: descriptive text
  - Type: "Feature List Card" — White background with rounded gray band
````
*来源：https://note.com/yoshifujidesign/n/n7412bccb5762*

---

## Sports / Athletic / Energy

**风格**：运动激情·深色背景·霓虹绿橙点缀·斜切形状

![Preview](https://hackmd.io/_uploads/BJChHgFGZx.png)
![Preview](https://hackmd.io/_uploads/SkQ6BgFzZg.png)

````
# presentation_design_spec_sports_active_jp.yaml
# Style: Sports / Athletic / Energy
# Concept: "Speed, Impact, and Heartbeat"

Global Design Settings:
  Tone: "Passionate, fast-paced, powerful, competitive"

  Color Palette:
    Base: "#111111 (asphalt-like black)"
    Text: "#FFFFFF (white)"
    Accent:
      - "#CCFF00 (Bolt Lime)"
      - "#FF4500 (Neon Orange)"
    Gradient: "Overlay a black-to-transparent gradient on top of photos"

  Typography:
    Headings: "Extra-bold italic gothic type (Impact, Din Condensed, etc.)"
    Body: "Italic sans serif type"
    Numbers: "Stencil-style or jersey-style sports typography"

  Common Layout Rules:
    Navigation: "Place page numbers inside angled, diagonal-cut shapes"
    Shapes: "Skew rectangles or images, or use parallelogram shapes"

Layout Variations:
  - Type: "Action Cut" — Dynamic background photography with large italic text overlapping
  - Type: "VS Layout" — Diagonal screen division, your side vs competitor
  - Type: "Speed Meter" — Metrics displayed as car speedometer or scoreboard
  - Type: "Highlight Stripe" — Bold diagonal stripe behind key words
````
*来源：https://note.com/yoshifujidesign/n/n7412bccb5762*

---

## Classic / Pop (Sculpture × Vaporwave)

**风格**：古典大理石雕塑×现代霓虹波普·高饱和度

![Preview](https://hackmd.io/_uploads/ByC4UltzWg.png)
![Preview](https://hackmd.io/_uploads/B1zB8lFG-e.png)

````
# presentation_design_spec_sculpture_pop_flexible_jp.yaml
# Style: Sculpture Pop Art / Vaporwave / Neon Surrealism
# Concept: "A Free Remix of Classical Art and Modern Pop Objects"

Global Design Settings:
  Theme: "Classical marble sculpture × modern neon pop (flexible style)"
  Tone: "Bold, humorous, high-saturation, fashionable, surreal"

  Visual Identity:
    Background Colors: "High-saturation solid colors that change each slide (cyan, magenta, yellow, lime, purple, etc.)"
    Collage Materials:
      Sculptures: "Various classical white marble statues (change per slide)"
      Gadgets: "Modern pop items (sunglasses, headphones, smartphones, VR, food items)"
      Item Colors: "Adjust each object to be complementary or analogous to background"

  Typography:
    Headings: "Ultra-bold sans serif (e.g., Helvetica Now Display Black)"
    Text Color: "Whichever color achieves highest contrast with background"

Layout Variations:
  - Type: "Drink Vibes (Cover)" — Bust wearing colorful sunglasses, sipping juice
  - Type: "Bubblegum Shock" — Statue blowing large bubblegum bubble
  - Type: "Music Head" — Statue wearing colorful headphones on dark background
  - Type: "Scream Color" — Statue with expressive pose on bright background
  - Type: "Split Duality" — Screen divided into two contrasting colors
  - Type: "Selfie King" — Statue taking selfie with SNS-style UI on phone screen
  - Type: "VR Dive" — Statue wearing VR goggles with floating 3D objects
  - Type: "Donut Chart" — Use real donut/pizza photos to build chart
  - Type: "Item List" — Statue holding pop items with speech bubbles
  - Type: "Comparison (A vs B)" — Two statues facing each other, Old vs New styled
  - Type: "Team Pedestal" — Multiple busts on pedestals as team members
  - Type: "QR Contact" — Statue with QR code sticker as ending slide
````
*来源：https://note.com/yoshifujidesign/n/n7412bccb5762*

---

## Tech / Art / Neon

**风格**：构成主义·科技艺术·暖灰底+霓虹黄·建筑蓝图感

![Preview](https://hackmd.io/_uploads/BJOY8ltzWx.png)
![Preview](https://hackmd.io/_uploads/r11cIlYfbx.png)

````
# presentation_design_spec_neon_collage_jp.yaml
# Style: Constructivism / Tech-Art / Avant-Garde
# Concept: "Architecture of Intelligence"

Global Design Settings:
  Tone: "Avant-garde, structural, intellectual, artistic, future-oriented"

  Visual Identity:
    Background Color: "Warm gray / beige (#E0E0D0) — matte, paper-like texture"
    Text Color: "Charcoal gray (#333333) — not pure black"
    Accent Color: "Neon Yellow (#DFFF00) — used for geometric shapes"
    Line Color: "Ultra-thin gray lines (0.5pt), similar to architectural draft lines"

  Typography:
    Headings: "Mix of serif (Didot, Bodoni) and sans serif (Helvetica)"
    Body: "Small-size text aligned strictly to the grid"
    Numbers: "Typewriter-style fonts (Courier New)"

Slide Composition Patterns:
  - Type: "Triple Collage (Cover)" — Screen divided into three sections with grid lines
  - Type: "Technical Drawing (Analysis)" — Fine grid background with line-art illustrations
  - Type: "Geometric Connection (Process)" — Neon yellow circles, squares, triangles with dotted lines
  - Type: "Radar Chart Art (Data)" — Large spiderweb-style radar chart across slide
````
*来源：https://note.com/yoshifujidesign/n/n7412bccb5762*

---

## Anti-Gravity / Artifact Deck

**风格**：反重力器物·极简空气感·蓝紫渐变·Apple/DeepMind 风格

![Preview](https://hackmd.io/_uploads/B1EVPrCfWl.png)
![Preview](https://hackmd.io/_uploads/rk4DDBAMbx.png)
![Preview](https://hackmd.io/_uploads/ryN4Dr0zbl.png)

````
Style Name: Anti-Gravity / Living Artifact Presentation

1. Core Concept
This presentation is not a slide deck. It is a living artifact.
Visualizes thinking becoming structure. Feels like an interface for ideas.
Calm, modern, confident, precise. Built for agents, systems, and future workflows.

2. Overall Aesthetic
Minimal, airy, high negative space, no visual noise.
Emotion: "This system already works. We are just showing you."

3. Background & Canvas
Pure white background as default.
Add soft, flowing gradient accents: Blue → cyan → violet, very low opacity.
Gradients feel like light, motion, energy, anti-gravity fields.

4. Typography System
Clean, modern sans-serif with slightly rounded geometry. Medium-bold weight.
Language: (the language should be what users said in the prompt) primary, English secondary labels.

5. Color System
Primary text: Black or very dark gray.
Accent: Calm blue, used sparingly for headlines, arrows, key icons.

6. Layout Language
Left-aligned, clear reading flow, wide margins, lots of white space.
Common: Text on left, visual on right; three-column feature cards; one idea per slide.

7. Visual Metaphors
- Thought → Structure: Messy scribble → arrow → clean diagram
- Interface as Proof: Realistic browser/app screenshots
- Cards as Capabilities: Soft rounded rectangles, subtle shadows

8. Iconography: Thin-line outline style, consistent stroke weight.

9. Tone of Copy: Clear, precise, slightly philosophical. No hype language.

10. What to Avoid (Strict): No pixel art, no thick borders, no bright blocks, no collage, no stickers.
````

---

## Deformed Flat Persona

**风格**：扁平变形人设·厚轮廓·柔和色调·纯色背景

![Preview](https://hackmd.io/_uploads/r1HEH0um-x.jpg)
![Preview](https://hackmd.io/_uploads/SkqEB0dQZl.jpg)
![Preview](https://hackmd.io/_uploads/Ska4SCdXZl.jpg)

```
# Style:
- Flat colors

# Illustration:
- A person with slightly deformed form
- Thick outlines

# Color:
- Gentle tones with a bit of white mixed in
- Up to 3 colors allowed

# Outline:
- Thick

# Background:
- Solid flat color with 1 color
```
*来源：[Kawai](https://x.com/kawai_design)*

---

## Neo-Retro Dev Deck

**风格**：复古未来主义·像素信息图·开发者中心·工程笔记本感

![Preview](https://hackmd.io/_uploads/HykAwBRf-l.png)

````
Style Name: Neo-Retro Dev Deck / Pixel-Infographic Editorial

1. Core Visual Identity
Aesthetic: Retro-futuristic, developer-centric, editorial infographic style
Feels like: 90s computer manuals × modern AI dev tools marketing × pixel-art meets startup slide deck
Mood: Confident, playful, opinionated, slightly rebellious

2. Canvas & Background
Light cream / off-white grid paper background, subtle square grid (engineering notebook feel)

3. Typography System
Primary headline: Bold, heavy sans-serif, slightly condensed, high contrast.
Headlines can be (the language should be what users said in the prompt) + English mixed.

4. Color Palette (Strict)
Hot Pink (agent / intelligence concepts)
Bright Yellow (editor / code / tools)
Cyan / Light Blue (browser / web / execution)
Black (text, borders)
White / cream (background)

5. Layout Language
Stacked modular blocks, rectangles with thick black borders, slight overlaps allowed.

6. Iconography
Pixel-art style icons: Rocket, robot, gear, code brackets, browser window, chat bubbles.
8-bit or 16-bit inspired, flat colors, black outline.

7. What to Avoid
No gradients, no realistic photos, no soft shadows, no corporate templates.
````

---

## 源仓库

所有提示词均来自 [awesome-notebookLM-prompts](https://github.com/serenakeyitan/awesome-notebookLM-prompts) · CC BY 4.0 许可
