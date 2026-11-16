# Product Requirements Document: Dark Theme

## Overview

Add an optional dark theme to the existing Memory Game so players can switch between light and dark appearances while playing. The change is limited to presentation and must not alter gameplay.

## Goals

- Let players switch themes with a clearly labeled, keyboard-accessible control.
- Remember the selected theme in the browser across page reloads.
- Keep the current light appearance as the default for players without a saved preference.
- Maintain readable contrast and visible focus indicators in both themes.

## User stories

- As a player, I want to turn on a dark theme so I can play with a darker interface.
- As a player, I want my theme choice remembered when I return.
- As a keyboard user, I want to reach and activate the theme control without a mouse.

## Requirements

1. Add a native button labeled "Dark theme" to the game header. Its `aria-pressed` state reflects whether dark theme is active.
2. Activating the button switches the page between light and dark themes without resetting the board, score, timer, or selected grid size.
3. Use CSS custom properties for theme-dependent page, text, panel, card, and button colors. Keep the existing light theme colors and layout as the default.
4. Persist the theme under a separate local-storage key so existing best scores remain unchanged.
5. Apply the saved theme when the page loads. If no dark preference is saved, use the existing light theme.
6. Preserve the current responsive layout, card interactions, keyboard play, animations, scoring, and win flow.

## Acceptance criteria

- The game starts in its existing light appearance when no theme has been selected.
- The theme button switches the page to dark and back; its pressed state stays in sync.
- Reloading the page retains the last selected theme.
- Theme changes do not reset or otherwise change the active game or saved high scores.
- The game remains usable at both grid sizes and on narrow screens.
- The theme control is a keyboard-focusable native button, and focus remains visible.

## Out of scope

- Automatically following the operating system theme.
- Changing game rules, card designs, score behavior, or adding new dependencies.
