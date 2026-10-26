# Gentle

![Gentle app banner](./assets/gentle-banner.svg)

**A calm, beautifully simple space for your thoughts.**

Gentle is a rich-text writing app for Windows and the browser. It pairs a distraction-light editor with eight color themes, straightforward document tools, and OpenDocument Text (`.odt`) support.

## Features

- **Eight color themes:** Rosewater, Lavender, Sky, Sage, Berry Dusk, Amethyst, Midnight, and Evergreen. Your theme choice is remembered.
- **Rich-text formatting:** Bold, italic, underline, strikethrough, headings, lists, quotes, alignment, links, and adjustable line spacing.
- **Document controls:** Create a document, edit its name, open an `.odt`, and save to `.odt`.
- **Images:** Insert images from a file, paste them from the clipboard, or drag them into the page. Images are embedded when saved to `.odt`.
- **Editing tools:** Undo, redo, and keyboard shortcuts for common formatting actions.
- **Desktop app:** A Windows installer creates Start menu and desktop shortcuts. Documents are stored on your device.

## Get started

### Run in a browser

Requires Node.js 18 or newer.

```sh
npm install
npm run dev
```

Open the local address printed by Vite. Browser mode uses the browser’s file picker and download for opening and saving documents.

### Run as a desktop app

```sh
npm install
npm run desktop:dev
```

### Build the Windows installer

```sh
npm install
npm run desktop:build
```

Installers are organized by version under `release/Gentle/v<version>/`. For example, version `1.0.2` is built to `release/Gentle/v1.0.2/`. Share the `.exe` installer; the accompanying `.blockmap` is not needed for a normal installation.

Build artifacts are excluded from Git. To distribute a release on GitHub, upload the generated `.exe` to a GitHub Release.

New releases stay on the `1.0.x` series by incrementing the patch version in `package.json` before building.

## Keyboard shortcuts

| Action | Shortcut |
| --- | --- |
| Bold | `Ctrl+B` |
| Italic | `Ctrl+I` |
| Underline | `Ctrl+U` |
| Undo | `Ctrl+Z` |
| Redo | `Ctrl+Shift+Z` |

## Built with

React · TypeScript · Material UI · TipTap · Electron · Vite

## Project layout

```text
electron/       Desktop window and secure file dialogs
scripts/        Versioned installer organization
src/            React editor, themes, styles, and ODT support
assets/         Repository artwork
```
