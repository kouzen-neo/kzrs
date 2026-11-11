# Changelog

All notable changes to KZRS, newest first.

## 1.0.1 (2026-11-11)

### Faster translation
- About three times faster on a typical chapter: up to 3 requests go to the AI at once
  (Settings > AI provider > At once, 1 to 8), a translated batch is cleaned and lettered, three
  pages at a time, while the next one waits for the AI, and the batch after that is detected
  meanwhile.
- Bubbles the AI deliberately skips (credits, watermarks, name tags) are no longer sent again.
- Optional light model: small bubbles and short lines can go to a cheaper model of the same
  provider (Settings > AI provider > Light model); the main model takes anything it misses.
  It saves on an expensive main model; it does not make a chapter faster.
- Fewer "too many requests" errors on free API plans: KZRS sends at most 12 requests a minute
  to Google Gemini (its free plan allows about 15) and waits when it gets there. A dialog says
  why a chapter is waiting and lets you turn the limit off; set it for any provider in
  Settings > AI provider > Per minute.
- Retry failed pages: when a few pages fail (a rate limit, a timeout), one click sends only those
  again and keeps the pages already done.

### Consistent names
- The AI now reports the character names, places and terms it meets. Names a series keeps using
  (seen in 2 of its chapters) are spelled the same way in its next chapters. They are listed in
  the Glossary, where you can keep them as glossary terms or forget them.
  Turn it off in Settings > Prompt > Learn character names.

### A new look
- One menu button, a grouped Translate panel, recent projects with covers and hover actions.
- Translation progress shown on the pages themselves, skeleton thumbnails while they load,
  toasts for finished work and errors, softer dialogs.
- Find anything with Ctrl+K: modes, actions and projects.
- Accent colors (Amber, Blue, Violet, Green, Rose) in Settings > General.
- The editor's tools are grouped with richer tooltips, the inspector is aligned, and the zoom
  sits in a floating pill on the page.
- The app icon's ".rs" tag is amber, like the app.

### First start
- A three-step welcome: target language, AI provider (with a connection test, and the base URL
  and model for a custom server), then your first pages.
- Google Gemini is the default provider for new installs.

### Updates
- KZRS checks GitHub once a day for a newer version and says so; Help > Check for updates
  asks right away.

## 1.0.0 (2026-11-06)

First public release, for Windows and Linux. macOS is coming soon.

### Translate
- Translate images, folders, ZIP / CBZ, EPUB and PDF; each run becomes a project you can reopen.
- Bubble and free-text detection, OCR, inpainting and typesetting run on your computer; only the text
  goes to the translation provider.
- Providers: Google Gemini, Anthropic Claude, OpenAI, OpenRouter, Zen, OpenCode Go and any
  OpenAI-compatible endpoint (Ollama, LM Studio, vLLM...). Glossary and prompt options.
- LaMa (optional download) or fast Telea inpainting; five bundled comic fonts or your own.

### Editor
- Move, resize, rotate and restyle text boxes; oval boxes; multi-select, copy and paste.
- Style presets (Dialogue, Shout, Thought, Narration, SFX and your own), inline bold and italic,
  letter case, line and letter spacing.
- Brush, restore and erase tools, Erase area, pictures and layers, batch edit, undo and redo per page.
- The mouse wheel over a number field or slider changes it a step per notch.

### Reader and export
- Page and webtoon reading; export to CBZ or PDF.

### Free and Supporter
- Free: 10 translated pages and 5 manual (editor-only) pages a day; editing, reading and exporting
  what you already have are not limited.
- Supporter: no daily limits, plus the command line and the AI agent tools (MCP) for Claude Code,
  OpenCode and Codex. One code, one computer, 1 year or 3 years.

### Downloads
- Windows setup `.exe` (no admin needed) and `.msi`, Linux AppImage and `.tar.gz` (Ubuntu 24.04,
  Debian 13, Fedora 39, Mint 22 or newer).
- macOS `.dmg` (Apple Silicon): coming soon.
