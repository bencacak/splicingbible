# 🔆 Fiber Optic Color Chart Builder

An interactive, browser-based splice planning tool built around the **TIA-598-D** color code standard. No installation, no server, no dependencies — open `index.html` and go.

**[Documentation](https://bencacak.github.io/splicingbible/docs.html)**

---

## What it does

Drop in a fiber count (6 to 1728 fibers), assign splice count labels to fiber positions, and get a fully color-coded chart you can export or share. Everything runs locally in the browser — your data never leaves your machine.

## Features

- **TIA-598-D color chart** — visual fiber map for any standard cable size, with correct 12-color cycling across ribbons and tubes
- **Flexible count assignment** — row-by-row form input or bulk paste (`LABEL,N-M` format)
- **Dead fiber support** — mark positions as dead/dark using `XD`, `D`, or `dead`
- **Click-to-assign** — click any fiber cell for individual overrides
- **Color Sync** — auto-aligns assignments to TIA color group boundaries
- **Tube View** — groups ribbons into super-bundles for cables ≥ 432 fibers
- **Fiber lookup** — type a position number to find its assigned count instantly
- **Dark & light themes** — persisted via `localStorage`
- **Four export formats** — Save Web Page (full state snapshot), PNG, PDF, Print

## Export & Saving

| Format | Best for |
|---|---|
| 💾 Save Web Page | Sharing a full interactive snapshot — opens with all data restored |
| 📷 PNG | Embedding in emails, wikis, or tickets |
| 📄 PDF | Print-ready documents with header metadata |
| 🖨️ Print | Direct printing (use light theme for ink economy) |

## Usage

```
# No build step required — just open the file
open index.html
```

Assign counts in the sidebar panel, press **Apply to Chart**, then export. See the **[full documentation](https://bencacak.github.io/splicingbible/docs.html)** for a complete walkthrough.

## Standard Reference

This tool implements **ANSI/TIA-598-D**, the North American standard for optical fiber cable color coding. The 12-color sequence (Blue → Orange → Green → Brown → Slate → White → Red → Black → Yellow → Violet → Rose → Aqua) repeats for each ribbon and tube group.

## Dependencies

All loaded from CDN — no local install needed.

- [`html2canvas`](https://html2canvas.hertzen.com/) — PNG/PDF capture
- [`jsPDF`](https://github.com/parallax/jsPDF) — PDF generation
