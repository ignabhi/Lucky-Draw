# 🎉 Lucky Draw — Philips TVM Fun League '26

A polished, single-file web app that picks a random winner from a list of names with a suspenseful, animated spin. Built for the **Qlipse Committee** to run live lucky draws at events.

> Upload a spreadsheet, hit **Draw Winner**, and watch the reel tease the crowd with fake-out stops before revealing the winner in a celebratory modal.

## ✨ Features

- **One-click draw** — a big central button spins through names and lands on a random winner.
- **Fair & secure** — winners are chosen with `crypto.getRandomValues` (cryptographically secure randomness), independent of row order.
- **Fake-out suspense** — 1–2 randomized "fake stops" tease the audience before the real reveal.
- **Winner modal** — the name pops in a beautiful gradient-bordered card with a confetti burst and gentle confetti rain.
- **Excel / CSV upload** — reads `.xlsx`, `.xls`, and `.csv` files (drag & drop supported) via SheetJS.
- **Smart column detection** — auto-finds the `Name` column, with a manual override dropdown.
- **Exclude previous winners** — on by default, so nobody wins twice (toggleable).
- **Live stats** — Names / Remaining / Drawn counters.
- **Keyboard shortcut** — press **Space** or **Enter** to draw.
- **Present mode** — one-click **Fullscreen** button for projectors.
- **Reset round** — clear drawn winners and start fresh without re-uploading.
- **Responsive** — fits any screen with no scrolling (uses dynamic viewport units).

## 🚀 Usage

1. Open the app (see **Live Demo** below, or open `index.html` locally).
2. Click **Upload the List** (or drag a file onto it).
3. Confirm the detected **Name column** if needed.
4. Press **Draw Winner** (or hit **Space** / **Enter**).
5. The winner appears in the modal — press **Draw Again** for the next round.

## 📄 Input format

Provide a spreadsheet with a header row. The app auto-detects a column named **Name** (also matches `Employee`, `Player`, `Participant`, etc.). Extra columns are ignored.

| SLNo | Name           | Email                      |
|------|----------------|----------------------------|
| 1    | Aarav Menon    | aarav.menon@philips.com    |
| 2    | Divya Nair     | divya.nair@philips.com     |

Blank rows and duplicate names are removed automatically.

## 🛠️ Tech

- Plain **HTML / CSS / JavaScript** — no build step, no framework.
- [SheetJS (xlsx)](https://sheetjs.com/) via CDN for spreadsheet parsing.
- Canvas-based confetti and CSS animations.

Everything lives in a single [index.html](index.html) file.

## 🌐 Live Demo (GitHub Pages)

Once GitHub Pages is enabled for this repo (Settings → Pages → Deploy from branch → `main` / root):

**https://ignabhi.github.io/Lucky-Draw/**

## 🧑‍💻 Run locally

Just open the file in a browser:

```powershell
Start-Process "index.html"
```

No server or dependencies required (an internet connection is needed once to load the SheetJS CDN).

## 💜 Credits

Made by the **Qlipse Committee** · Philips TVM Fun League '26.
