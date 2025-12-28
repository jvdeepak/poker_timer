# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Poker Tournament Timer** - a single-file web application built with vanilla HTML5, JavaScript, and CSS3. The entire application lives in `poker_timer.html` (~2,200 lines) with zero external dependencies.

## Development

**No build system required.** Open `poker_timer.html` directly in a browser to run. Changes take effect on page refresh.

Browser compatibility: Chrome, Firefox, Safari, Edge.

## Architecture

The application is a self-contained SPA organized into functional sections within a single `<script>` block:

### State Management
Global variables manage all application state:
- `structure[]` - Array of blind level objects (smallBlind, bigBlind, ante, duration)
- `currentLevelIndex`, `timeRemaining`, `totalSeconds` - Timer state
- `playersRemaining`, `rebuys` - Tournament tracking
- `isRunning`, `soundEnabled`, `presentationMode` - UI state flags

### Key Functional Areas (by line ranges)
- **Configuration** (~1176-1204): Default chip definitions, initial state
- **Presets** (~1209-1333): 6 tournament structures (Turbo, Standard, Deep Stack, Super Turbo, Shootout, Bounty)
- **Audio System** (~1338-1395): Web Audio API for alerts/beeps
- **Display/Rendering** (~1397-1540): `updateDisplay()`, `updateStats()`, `updatePrizePool()`
- **Timer Control** (~1538-1650): `startTimer()`, `pauseTimer()`, `advanceLevel()`
- **Player Management** (~1668-1750): Player tracking, rebuy handling
- **Presentation Mode** (~1711-1730): Full-screen TV/projector display
- **Structure Management** (~1754-1846): Blind level editing
- **Import/Export** (~1889-1939): JSON tournament persistence
- **Settings Persistence** (~2015-2110): localStorage auto-save
- **Event Handling** (~2123-2193): Keyboard shortcuts, initialization

### Data Persistence
Uses `localStorage` with key `'pokerTimer'`. Auto-saves every 30 seconds and on page unload.

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Space | Start/Pause timer |
| N | Next level |
| P | Previous level |
| R | Reset current level |
| F | Toggle fullscreen |
| T | Toggle presentation mode |
| S | Toggle sound |
| +/- | Adjust player count |
| A | Add rebuy |
