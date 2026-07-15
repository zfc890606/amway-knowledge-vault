---
name: markitdown
description: Convert various file formats (PDF, DOCX, PPTX, XLSX, images, audio) to clean Markdown using Microsoft's MarkItDown. Ideal for preparing documents for LLM processing.
---

# MarkItDown - File to Markdown Converter

Convert files to clean, token-efficient Markdown for LLM processing. Uses Microsoft's open-source MarkItDown library.

## Supported Formats

- **Documents**: PDF, DOCX (Word), PPTX (PowerPoint), XLSX (Excel)
- **Media**: Images (JPEG, PNG, GIF, WebP) — with OCR for text extraction
- **Audio**: WAV, MP3 — with speech transcription
- **Web**: HTML, CSV, JSON, XML, ZIP, EPUB
- **Other**: YouTube URLs (fetch transcripts)

## Installation

```bash
pip install 'markitdown[all]'
```

Or for minimal install:
```bash
pip install markitdown
```

## Usage

### CLI
```bash
markitdown input.pdf > output.md
markitdown input.docx > output.md
markitdown image.png > output.md
```

### Python API
```python
from markitdown import MarkItDown

md = MarkItDown()
result = md.convert("document.pdf")
print(result.text_content)
```
