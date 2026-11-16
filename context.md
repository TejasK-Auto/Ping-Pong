# Repository Context

## What this project does

This repository contains a small, standalone Memory (also known as Concentration) game. A player flips cards to find matching emoji pairs, aiming to finish with as few moves as possible. The game offers 4x4 and 6x6 boards and tracks moves, elapsed time, and a star rating.

When a game is completed, its score is saved in the browser's local storage, and the best five scores are displayed. The game can be played with a mouse or keyboard.

## How it is built

The application is implemented in `memory-game.html` using plain HTML, CSS, and JavaScript. Styles and game logic are embedded in that file; there are no external libraries, build tools, or dependencies. The responsive layout uses CSS Grid, and the cards use CSS transforms for their flip animation.

To play, open `memory-game.html` in a modern browser. Alternatively, serve the repository directory with a local HTTP server and open the file through that server.

## What the name stands for

“Memory Game” describes the game itself. The repository name includes the suffix “GHCP,” but the project files do not define what that suffix means, so its intended expansion is unknown.

## Project intent

The implementation presents a lightweight, accessible, dependency-free browser game. Its keyboard interaction, responsive board, and persistent local scores make it usable without a separate account or backend.
