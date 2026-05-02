# 🍄 Mario Chess 🏰

A Mario-themed two-player chess game with a built-in chess clock, full rules, and retro HUD styling. Installable as a Progressive Web App and deployed via GitHub Pages.

**▶️ Play it:** https://joahg.github.io/mario-chess/

![Mario Chess](icons/icon-512.png)

## Features

- ♟️ **Full chess rules** — castling (both sides), en passant, promotion, check, checkmate, stalemate, draw by insufficient material, threefold repetition, and the 50-move rule.
- 🍄 **Mario theme** — Mushroom Kingdom pieces vs. Bowser's army, ?-block + brick board, green-pipe border, sky/clouds/hills background.
- ⏱️ **Chess clock** — 5 / 10 / 15 / 30 minute controls with optional 0/2/5s increment. Pulses red and ticks audibly under 30s.
- 🎵 **Synthesized retro sounds** for moves, captures, check, castle, promotion, and checkmate (mute toggle included).
- 🎯 **Move helpers** — legal-move highlighting, last-move indicator, in-check pulse, captured pieces panel, algebraic move list.
- 🔁 **Undo, pause, new game**, and a game-over modal with coin confetti.
- 📱 **Installable PWA** with offline support via service worker.

## Controls

| Action | Control |
| --- | --- |
| Select / move piece | Click or arrow keys + Enter |
| Deselect | Esc |
| Pause / resume clock | Space |
| Undo | U |

## Run locally

It's a single static page — any local server works:

```bash
cd mario-chess
python3 -m http.server 8000
# then open http://localhost:8000/
```

> Service workers require `http(s)://` (or `localhost`); they won't register from `file://`.

## Project structure

```
mario-chess/
├── index.html              # The whole game (HTML + CSS + JS)
├── manifest.webmanifest    # PWA manifest
├── sw.js                   # Service worker (offline cache)
├── 404.html                # SPA-style fallback for GitHub Pages
├── icons/
│   ├── favicon.svg
│   ├── favicon-32.png
│   ├── apple-touch-icon.png
│   ├── icon-192.png
│   ├── icon-512.png
│   └── icon-maskable-512.png
└── .github/workflows/pages.yml   # Auto-deploy to GitHub Pages
```

## Deployment

Pushed to `main` automatically deploys to GitHub Pages via the included workflow.

## License

MIT
