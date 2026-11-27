# Changelog

All notable changes to Kazeru (formerly KZRS), newest first.

## 1.1.0 (2026-11-22)

### macOS
- KZRS for macOS: `KZRS-1.1.0-macos-arm64.dmg` for Apple Silicon Macs (M1 to M5) with macOS 13.4
  or newer, added to this release on 2026-11-24. Shortcuts use Cmd and Option, and the menus and
  tips show them that way; Ctrl+Cmd+F switches the Reader to fullscreen.

### Speech bubbles and formatting
- Drawn speech bubbles under a box's text: Box, Rounded, Oval, Thought or Shout, with fill,
  outline, padding and a tail you aim with its own handle. They cover lettering that is hard to
  erase. The Bubble tool (U) puts one under a box, or makes a new box with one.
- Format part of a line: bold, italic, text colour, outline, font and size, from a toolbar over
  the Translation field (or tags such as `<b>`, `<c=red>`, `<s=150%>` typed in the text). The
  field shows the tags small and dim. The old `**bold**` and `*italic*` still work.
- The format menus open beside the panel, so the text and its selection stay in view.

### Your own fonts
- Add font... at the end of every font list (options bar, format toolbar, batch edit) imports TTF,
  OTF, TTC/OTC (every font in it), WOFF, or a ZIP of them. ZIPs are searched through all their
  folders, ZIPs inside ZIPs included, so a font bundle comes in at once; other files are left out.
- Imported fonts are kept by KZRS, named from the font itself ("Anime Ace Bold"), listed with a
  preview in their own lettering, and work in `<f=...>` tags. A font already there is not added
  twice; right-click one of your fonts in a list to remove it.
- Opening a page that names a font this computer does not have says so; it draws in Default.

### Editing faster
- Pages renamed in a file manager keep their edits: opening the chapter (or renaming while it
  is open) matches each page to its new file, so the editor no longer shows a black or wrong
  page and saving no longer writes the old name again (a duplicate page). A page whose file is
  gone shows its clean page in the Pages panel.
- Restore original: right-click a box (or several) to bring back the original page under them
  and remove those boxes, or empty page space to restore the whole page and remove all its text.
  One step, undone with Ctrl+Z.
- Deleted pages: Ctrl+Z right after Delete page puts the page back; later, the trash button in
  the Pages panel (or Deleted pages in a page's menu) lists them to restore, or empties the trash.
- Close (Ctrl+W, File menu, or the X in the Pages panel and the Reader bar) closes the chapter
  and shows the start screen.
- New project takes a PDF, CBZ, ZIP, EPUB or folder as well as images (one project per book or
  folder). Open project folder starts in the output folder instead of the home folder.
- `.kzrs` project files: Export as .kzrs project (Projects menu or File) packs the pages and their
  edit data into one file; File > Open, Open .kzrs file in Projects, dropping it on Projects or
  Open with KZRS unpacks it beside the chapters of its language and opens it in the editor.
- File menu: Translate pages, New project, Open (a .kzrs project, a book or an image)
  and Open folder (a project opens in the editor, other pages in the Reader). Projects explains
  its buttons, and Open project folder on a plain image folder starts a new project.
- CBZ and PDF exports of a project take only its pages, not copies or extra images in the folder;
  a failed CBZ export leaves no half-written file.
- File names work the same on Windows, macOS and Linux: images in ZIP and CBZ files with
  characters Windows forbids are unpacked with "_", and renaming a page to a different case
  works on Windows and macOS.
- Rename or delete a page from its right-click menu in the Pages panel (a duplicate page, a
  wrong name). The page's file and its edit data change together; a deleted page goes to the
  chapter's `.kzrs/trash/` folder, so it can still be put back.
- Select by rectangle: Ctrl+drag over the page selects every box and picture the rectangle
  touches; Shift+drag on empty page adds them to what is already selected.
- Translate area (A): drag over lettering and it becomes a box with its translation. Dragged over
  a box that is already there, it replaces that box and keeps its style instead of adding a
  second translation.
- Proofread by keyboard: Enter types over the selected box's text; while typing, Tab goes to the
  next box's text and on to the next page, Shift+Tab back.
- F4 repeats the last style change (colour, size, bubble...) on the selected boxes.
- Translate with a note (right-click a box): the AI translates it again following a short
  instruction such as "more casual" or "keep the name Kei"; recent notes are offered again.
- Continue: the empty editor (and Ctrl+K) opens the chapter and page you last edited.
- Edit a chapter while it is still translating: Edit opens the pages done so far; the others
  join the page list as they finish.
- Page Up / Page Down open the next page almost at once: the pages next to the open one are
  prepared ahead.
- The AI models used for erasing and finding bubbles load in the background when a chapter
  opens, so the first erase stroke does not wait for them. On a small computer (under 7 GB of
  memory or under 4 processor threads) they load when first used instead; Settings > Editor
  shows which way it works.
- Boxes you translate by hand are never skipped.

### Brush
- The Brush paints on its own layer under the text. Its new eraser takes off only what you
  painted, and the page shows again as it was, also after reopening the project. Clear paint
  removes all paint on the page. Paint made with earlier versions stays part of the page.
- Opacity (5 to 100%) replaces hardness: how much one stroke covers, or with the eraser how much
  paint comes off.

### Editor layout
- The inspector starts with an action bar (Translate, Erase, Find, Reset, Delete) and shows its
  settings as compact icon fields; the Layers list sits right under them.
- Tidier right-click menus with icons and shortcuts: one for a box, a picture, the page, and
  one for several selected items at once. Ctrl+A selects every box and picture.
- Tool rail in groups (select, paint, erase, lettering, pictures); the colour picker moved to
  the Brush options bar (I still picks).
- The page list numbers the pages and shows how many there are.
- Clearer icons, and "1 box" instead of "1 boxes".

### Reader, interface and translating
- Open PDF, CBZ, ZIP and EPUB files with KZRS from your file manager (Open with); they open in
  the Reader. KZRS is added as a choice, not made the default app. Also "Open book..." in the
  Reader and "Read a book" in the menu.
- Interface size: automatic on large screens (4K and 1440p at 100% scaling get a bigger
  interface), or pick 80 to 200% in Settings; Ctrl+Alt + / - / 0 change it.
- The page grid of a running translation marks every page being worked on (six at a time),
  not only the first.
- PDF export: pages of mixed resolution come out the same width.
- The Ctrl+K search no longer turns the screen dark over itself.

## 1.0.5 (2026-11-18)

### Buying a Supporter code
- Buy a code right in the app (Supporter activation > Buy a code): pick a plan, enter your
  email, scan the QRIS shown with any bank or e-wallet app. Once paid, the code activates itself;
  no receipt to send. The 0.7% QRIS fee is added to the price.
- Renew from Supporter > Renew…: the code stays the same and its end date moves on.
- A clearer Supporter screen: what Supporter adds on the left, the plans as cards with their
  price per month, and when active the code, end date and days left.
- The same purchase on the website (Supporter page). Discord is the community and the place to
  ask for help; the old QRIS picture and the #license receipt step are gone.

### Speed and accuracy
- Bubble detection about three times faster: the detector ran three times on every page (once per
  confidence stage); it now runs once and its result is filtered three ways. Same bubbles found.
- The detector model is half the size (52 MB instead of 104 MB): weights stored at half precision,
  same bubbles found.
- Local OCR reads vertical Japanese and Chinese correctly ("おい 待てよ！" was read as one wrong
  character) and is about a third faster: crops are read near their size on the page.
- Narration captions such as "Meanwhile..." are translated instead of skipped as credits.
- Big sound effects outside bubbles (such as "ドドド" or "ゴゴゴ" on screentone) are found: free text
  is detected on the page as it is, instead of with the bubbles blanked out first.
- Local OCR: a text the model leaves out twice (usually a credit line) is kept as SKIP instead of
  being sent again as a picture, which cost up to four extra requests per line.
- Rate limits: the wait Gemini asks for (`retryDelay`) is honoured, and with a per-minute cap a
  429 waits for the full minute.
- CLI: `--params` rejects unknown keys instead of ignoring them.
- Model downloads (OCR, LaMa) continue where they stopped: a dropped connection is retried from
  the bytes already saved, and an interrupted download continues next time instead of starting over.

### Reading bubbles
- Read bubbles: Auto, Vision or Local OCR (Settings > Translate). Auto checks once whether the
  chosen model can read images (a tiny picture of a digit) and uses vision when it can; a model
  that cannot gets the bubbles as text read on this computer by the OCR models. A model that
  refuses an image during a run is switched to OCR for the next pages.
- Test connection also says whether the model reads images.
- The editor's Translate again follows the same choice; boxes OCR cannot read are named in the log.
- Text outside bubbles is read once: the text found while detecting it is sent as is, so the
  OCR read mode no longer reads those boxes a second time.
- Starred sound-effect labels such as *BONK* stay separate from the dialogue next to them, so
  they are no longer erased together with it.
- The OCR prompt is now identical to the Android app's (checked by the parity test).
- Translate sound effects is on by default in the app (turned on once for existing settings;
  switching it off again keeps it off).
- Learned names no longer pick up whole lines of dialogue the AI listed by mistake; such
  entries from earlier chapters are left out of the prompt.

### Supporter
- New 3-month plan (Rp 10.000) next to 1 year (Rp 20.000) and 3 years (Rp 50.000).
- Free use is now 5 translated pages and 3 manual pages a day (was 10 and 5).
- The top bar chip shows the days left in the last 14 days of a plan, and the Supporter screen
  and Settings say how to renew (same code).

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
