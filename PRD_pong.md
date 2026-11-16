# Product Requirements Document: Pong

## Overview

Create a standalone browser version of Pong that can be opened and played from one HTML file. The game should preserve the quick, readable paddle-and-ball gameplay of the classic while supporting keyboard and touch-friendly controls.

## Goals

- Make a complete Pong match playable without installing dependencies or running a build.
- Offer a one-player mode against a computer opponent and a local two-player mode.
- Keep controls and scores easy to understand on desktop and mobile screens.

## User stories

- As a player, I want to play Pong against the computer.
- As two players sharing a device, we want to compete in a local match.
- As a player, I want to start, pause, resume, and restart a match.
- As a touch-screen player, I want on-screen controls for moving my paddle.

## Requirements

1. Deliver the game as `pong.html` with HTML, CSS, and JavaScript in the file and no external dependencies.
2. Provide one-player (left paddle vs. computer) and local two-player modes.
3. Use a first-to-seven scoring format. Show the current score and announce the winner when a player reaches seven points.
4. Provide a ready state before play, plus pause/resume and restart controls. Starting or restarting begins a fresh match.
5. In one-player mode, control the left paddle with W/S or the on-screen controls; the computer controls the right paddle.
6. In two-player mode, Player 1 uses W/S and Player 2 uses the Up/Down arrow keys. On-screen controls must also be available for each human paddle.
7. Keep paddles within the play area. The ball bounces off the top and bottom edges and paddles; a point is scored when it passes a paddle.
8. Adapt the play area to the viewport while maintaining a usable game layout on narrow screens.
9. Expose scores and game status as readable page text, label interactive controls, and support keyboard operation.
10. Add floating, visibly distinct collectibles in the paddle lanes. A paddle collects a power-up by overlapping it; one-player mode spawns them only in the human player's lane.
11. Include seven power-ups:
    - Big Paddle: temporarily enlarges the collecting player's paddle.
    - Paddle Boost: temporarily increases the collecting player's paddle speed.
    - Slow Ball and Speed Ball: temporarily change the ball speed for both players.
    - Curve Ball: temporarily curves the ball's path.
    - Shield: blocks one goal against the collecting player.
    - Shrink Opponent: temporarily reduces the other player's paddle size.
12. Show brief pickup/status messages and a power-up guide. Timed effects pause with the game and clear when a match is restarted or the game mode changes.
13. Keep the computer opponent beatable by limiting its paddle speed and using imperfect tracking.
14. On a desktop viewport, scale and compact the game layout so the match is visible without requiring page scrolling.

## Acceptance criteria

- Opening `pong.html` in a modern browser loads a playable game without network access or setup.
- The default one-player game can be started and played with W/S; the computer returns the ball.
- Two-player mode can be selected and both paddles can be controlled independently.
- On-screen paddle controls work with pointer/touch input.
- Pause, resume, and restart work without leaving an animation running while paused.
- Scoring resets the ball appropriately, and the first player to seven wins.
- The game remains playable at desktop and mobile viewport sizes.
- Each power-up can be collected in both game modes, and its effect or charge works as described.
- Pausing freezes the ball, power-up timers, and collectibles; restarting clears all active effects and pickups.
- A player can score against the computer without relying on power-ups.
- On a standard desktop browser viewport, the playfield and match controls fit on screen.

## Out of scope

- Online multiplayer, user accounts, leaderboards, and persistent match history.
- Sound effects, external images, and downloadable assets.
