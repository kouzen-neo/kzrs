<div align="center">
  <img src="docs/assets/app_icon.png" width="100" alt="Kazeru logo" />
  <h1>Kazeru</h1>
  <p><sub>formerly KZRS</sub></p>

  <p>
    <a href="https://github.com/kouzen-neo/kzrs/releases/latest"><img src="https://img.shields.io/github/v/release/kouzen-neo/kzrs?style=for-the-badge&color=f0a43a" alt="Latest release"></a>
    <img src="https://img.shields.io/badge/Windows-10%2F11-0078D4.svg?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
    <img src="https://img.shields.io/badge/macOS-Apple%20Silicon-000000.svg?style=for-the-badge&logo=apple&logoColor=white" alt="macOS">
    <img src="https://img.shields.io/badge/Linux-x86__64-FCC624.svg?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
    <img src="https://img.shields.io/badge/Rust-native-b7410e.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  </p>

  <p>
    <a href="README.md"><img src="https://img.shields.io/badge/EN-0078D4.svg?style=for-the-badge" alt="English"></a>
    <a href="README.id.md"><img src="https://img.shields.io/badge/ID-6e7681.svg?style=for-the-badge" alt="Bahasa Indonesia"></a>
  </p>
</div>

> **Legacy repository.** KZRS is now **Kazeru**. New releases, downloads and the changelog will move to [kouzen-neo/kazeru](https://github.com/kouzen-neo/kazeru) (not published yet). This repository stays online for the existing releases, and installed apps keep updating from it until the move.

Kazeru is a desktop manga and comic translator written in Rust. It finds the speech bubbles and
free text on a page with on-device AI, translates them with the LLM provider you choose (or a
local one such as Ollama or LM Studio), erases the original lettering and typesets the
translation back onto the page. A full page editor, a reader and CBZ/PDF export are built in.

This repository hosts the **releases** and the changelog; the source is private.

---

## Download

Get the latest version from **[Releases](https://github.com/kouzen-neo/kzrs/releases/latest)**.

| System | File | How to install |
|---|---|---|
| Windows 10/11 (64-bit) | `KZRS-Setup-<version>-x64.exe` | Run it and follow the steps (no admin needed). `KZRS-<version>-x64.msi` is the same app for IT / company PCs. |
| Linux x86_64 (Ubuntu 24.04, Debian 13, Fedora 39, Mint 22 or newer) | `KZRS-<version>-x86_64.AppImage` | Make it executable (`chmod +x`, or Properties → Allow executing) and open it. A `.tar.gz` with an `install.sh` menu installer is there too. |
| macOS 13.4 or newer (Apple Silicon: M1 to M5) | `KZRS-<version>-macos-arm64.dmg` | Open the `.dmg` and drag **Kazeru** to **Applications**. Intel Macs are not supported. |

The apps are not code-signed yet, so the system asks once:

- **Windows**: "Windows protected your PC" → **More info** → **Run anyway**.
- **macOS**: open Kazeru once, then **System Settings** → **Privacy & Security** → **Open Anyway**.
- **Linux AppImage**: if it does not start, install `libfuse2`, or run it with `--appimage-extract-and-run`.

The optional OCR and LaMa models download from inside the app the first time they are needed
(Settings > Models).

---

## Highlights

- **Many inputs**: images, folders, ZIP / CBZ, EPUB and PDF.
- **Local vision**: bubble detection, OCR, inpainting and typesetting run on your computer; the
  translation provider only gets the cut-out bubbles and text lines (one picture of them per
  request), never your whole pages or files.
- **Any LLM**: Google Gemini, Anthropic Claude, OpenAI, OpenRouter, Zen, OpenCode Go, or any
  OpenAI-compatible endpoint (Ollama, LM Studio, vLLM...).
- **Clean results**: LaMa / Telea inpainting, bubble-aware line breaking, vertical Japanese,
  bundled comic fonts and style presets.
- **Page editor**: move, resize and restyle boxes, drawn speech bubbles, bold / italic / colour /
  font / size inside a line, Translate area, brush with its own eraser, restore / erase tools,
  pictures and layers, batch edits, undo per page.
- **Reader and export**: page or webtoon reading, opens PDF / CBZ / ZIP / EPUB from your file
  manager, export to CBZ or PDF.
- **AI agents (Pro)**: an MCP server and a CLI, so Claude Code, OpenCode or Codex can
  check and fix pages for you.

---

## Free and Pro

Kazeru is free to use. Plans and buying a Pro code with QRIS (in the app or on the website): [kzrs.kouzen.my.id/supporter](https://kzrs.kouzen.my.id/supporter/).

---

## Feedback

Bugs and ideas: [Issues](https://github.com/kouzen-neo/kzrs/issues), or [Discord](https://discord.gg/CdZUeMQQK).

Changes per version: [CHANGELOG.md](CHANGELOG.md).

---

## License

Proprietary freeware. All rights reserved.
