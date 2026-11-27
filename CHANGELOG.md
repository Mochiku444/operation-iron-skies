# Changelog

All notable changes to **OPERATION: IRON SKIES** are documented here, newest first.
Future updates are collected under **Unreleased** as they are built, then dated when they ship.

## [Unreleased]

_Nothing yet — the next update lands here._

## [2026-11-27] — Start screen, portrait HUD, lobby polish

### Added
- Start screen: "click anywhere to start" is now a designed UI unit — a pulsing tap ring with an amber core and animated chevrons — inside a HUD box with amber corner brackets.
- Portrait touch layout (phones ≤560px wide): narrower objective box, gauge panel above the joystick, ROLL/BOOST as a bottom-right pair — verified zero overlapping elements in Mission and Free Flight.
- Compact touch mode for very short viewports (≤300px tall, e.g. browser URL bar visible): smaller joystick and radar, repositioned missile button.

### Changed
- Lobby: **Change Aircraft** is now a proper UI box — dark gradient panel, bright cyan border, amber corner brackets and icon — clearly visible against the hangar.
- Free Flight HUD is now identical to Mission mode; the floating End Sortie button is gone — ending a free/endless sortie lives in the pause banner (M key still works).
- Pause/Cam buttons slimmed down with a translucent glass background and moved directly under the objective box so they no longer block the view.

## [2026-11-26, evening] — Hangar lobby rebuild & balance

### Added
- Full-screen 3D hangar lobby: the selected jet idles on a glowing pad and can be drag-rotated; glass jet-info panel with stat pips and per-jet description; pilot mini-card.
- SELECT MISSION screen (missions appear only after ENGAGE MISSION), SELECT AIRCRAFT screen, and Armory / Service Record as their own full screens with Back to Hangar.

### Changed
- Enemy durability raised ~2.4×: fighters 110 HP, aces 220, ground base 220, ships 480, boss SKYHAMMER 1400.
- All in-game text is now in English.

### Fixed
- Inverted steering: stick left turned the jet right (bank→yaw sign); keyboard A/D had the same bug.
- Mobile panels cut off and unscrollable (safe-centering fix), joystick gestures stolen by the browser (`touch-action: none`, 0.09 dead zone, longer knob travel), pause banner now says TAP TO RESUME on touch and tapping it resumes.
- Touch HUD overlaps across several iterations; the final layout anchors the right column from the top so short viewports can no longer collide.

## [2026-11-26] — Initial release

### Added
- Single-file 3D fighter jet game (Three.js + Web Audio, no external assets): narration intro, 6-mission campaign, procedural jets, lock-on missiles, cannon, barrel roll, afterburner, upgrades (Armory), pilot ranks from Rookie to Phantom Legend.
- Persistent progress in localStorage (score, credits, unlocked missions, upgrades, selected jet, best Endless wave) with a two-click save reset.
- 3 selectable jets: F/A-07 Phantom (balanced), XF-09 Viper (fast, fragile), A-12 Juggernaut (slow, tank).
- Free Flight and Endless wave-defense modes.
- Pilot Service Record: 10 medals plus lifetime statistics (sorties, flight time, cannon accuracy, missiles fired, flawless missions, boss kills), with a new-medal notice on the debrief.
- Procedural building clusters across the theatres (Black Sea port skyline, Burning City towers, valley town, Asteria skyline on the Mission 01 horizon).
- Gameplay capture videos under `shots/`.
