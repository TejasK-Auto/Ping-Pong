# Browser Mini-Games

This repository contains two responsive, standalone browser games built with plain HTML, CSS, and JavaScript. No build step, external library, or network connection is required to play.

## Games

### Memory Game

Open `memory-game.html` to play. Choose a 4x4 or 6x6 board and find all matching emoji pairs.

- Mouse and keyboard play (Tab, then Enter or Space)
- Move counter, timer, and star rating
- Best five scores saved in browser local storage
- Optional dark theme; your theme choice is saved in browser local storage

### Pong

Open `pong.html` to play. The first player to score seven points wins.

- **1 Player:** Move the left paddle with W/S and play against the computer.
- **2 Players:** Player 1 uses W/S; Player 2 uses the Up/Down arrow keys.
- **Touch screens:** Use the on-screen paddle controls.
- Focus the playfield and press Space to pause or resume. Use the match buttons to start or restart.
- Move a paddle over a glowing pickup to collect its power-up. The game includes Big Paddle, Paddle Boost, Slow Ball, Speed Ball, Curve Ball, Shield, and Shrink Opponent.

The Pong computer opponent uses intentionally imperfect tracking. Open the in-game power-up guide for descriptions of the collectibles.

## Run locally

You can open either HTML file directly in a modern browser. Or serve the repository directory with Python:

```bash
python3 -m http.server 8000
```

Then open one of these URLs:

- `http://localhost:8000/memory-game.html`
- `http://localhost:8000/pong.html`

## Project files

- `memory-game.html` - Memory game
- `pong.html` - Pong
- `PRD_dark_theme.md` - Memory game dark theme requirements
- `PRD_pong.md` - Pong requirements
- `context.md` - Repository overview
