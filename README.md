<div align="center">
  <img src="docs/assets/app_icon.png" width="100" alt="KZRS logo" />
  <h1>KZRS</h1>

  <p>
    <a href="https://github.com/kouzen-neo/kzrs/releases/latest"><img src="https://img.shields.io/github/v/release/kouzen-neo/kzrs?style=for-the-badge&color=d9531e" alt="Latest release"></a>
    <img src="https://img.shields.io/badge/Windows-10%2F11-0078D4.svg?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
    <img src="https://img.shields.io/badge/macOS-11%2B-000000.svg?style=for-the-badge&logo=apple&logoColor=white" alt="macOS">
    <img src="https://img.shields.io/badge/Linux-x86__64-FCC624.svg?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
    <img src="https://img.shields.io/badge/Rust-native-b7410e.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  </p>

  <p>
    <a href="README.md"><img src="https://img.shields.io/badge/EN-0078D4.svg?style=for-the-badge" alt="English"></a>
    <a href="README.id.md"><img src="https://img.shields.io/badge/ID-6e7681.svg?style=for-the-badge" alt="Bahasa Indonesia"></a>
  </p>
</div>

KZRS is a desktop manga and comic translator written in Rust. It finds the speech bubbles and
free text on a page with on-device AI, translates them with the LLM provider you choose (or a
local one such as Ollama or LM Studio), erases the original lettering and typesets the
translation back onto the page. A full page editor, a reader and CBZ/PDF export are built in.

This repository hosts the **releases** and the changelog; the source is private.

---

## Download

Get the latest version from **[Releases](https://github.com/kouzen-neo/kzrs/releases/latest)**.

| System | File | How to install |
|---|---|---|
| Windows 10/11 (64-bit) | `KZRS-Setup-<version>-x64.exe` | Run it and follow the steps. `KZRS-<version>-x64.msi` is the same app for IT / company PCs. |
| macOS 11+ (Apple Silicon) | `KZRS-<version>-macos-arm64.dmg` | Open it and drag **KZRS** to **Applications**. |
| Linux x86_64 | `KZRS-<version>-x86_64.AppImage` | Make it executable (`chmod +x`, or Properties → Allow executing) and open it. A `.tar.gz` with an `install.sh` menu installer is there too. |

The apps are not code-signed yet, so the system asks once:

- **Windows**: "Windows protected your PC" → **More info** → **Run anyway**.
- **macOS**: open KZRS once, then **System Settings → Privacy & Security → Open Anyway**.
- **Linux AppImage**: if it does not start, install `libfuse2`, or run it with `--appimage-extract-and-run`.

The optional OCR and LaMa models download from inside the app (Settings > Storage).

---

## Highlights

- **Many inputs**: images, folders, ZIP / CBZ, EPUB and PDF.
- **Local vision**: bubble detection, OCR, inpainting and typesetting run on your computer; only
  the text of the bubbles goes to the translation provider, never the images.
- **Any LLM**: Google Gemini, Anthropic Claude, OpenAI, OpenRouter, Zen, OpenCode Go, or any
  OpenAI-compatible endpoint (Ollama, LM Studio, vLLM...).
- **Clean results**: LaMa / Telea inpainting, bubble-aware line breaking, vertical Japanese,
  bundled comic fonts and style presets.
- **Page editor**: move, resize and restyle boxes, brush / restore / erase tools, pictures and
  layers, batch edits, undo per page.
- **Reader and export**: page or webtoon reading, export to CBZ or PDF.
- **AI agents (Supporter)**: an MCP server and a CLI, so Claude Code, OpenCode or Codex can
  check and fix pages for you.

---

## Free and Supporter

KZRS is free with **10 translated pages a day**. The editor, reader and export are not limited.

A **Supporter** code removes the daily limit and unlocks the command line and the AI agent tools.
A code works on one computer for one year. To get one, contact the developer; the code arrives by
message and you activate it in the app (*Supporter activation*, or the chip in the top bar).

---

## Feedback

Bugs and ideas: [Issues](https://github.com/kouzen-neo/kzrs/issues).

Changes per version: [CHANGELOG.md](CHANGELOG.md).

---

## License

Proprietary freeware. All rights reserved.
