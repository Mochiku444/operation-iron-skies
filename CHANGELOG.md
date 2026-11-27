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
- Greener world with real mountains: Mission 01's airbase now sits in green country (grass ground, 20 hills, 160 scattered pines) ringed by tall peaks with snow caps on the highest; the valley (Mission 02) gained a mountain ring behind its hills, and the Black Sea coast (Mission 05) turned green with a mountain range behind the port.
- Fullscreen toggle: a ⛶ Fullscreen button on the start screen and in the pause banner — on phones this hides the browser chrome entirely, which also removes the short-viewport squeeze.
- A visible sun with god rays: a glowing sun disc sits at each sky's real sun direction, with a fan of additive light shafts that shimmer slowly — strongest at dawn (Mission 01), gentler by day and over the sea, and off at night.
- Cloud color now follows Rama's reference photo (a blue sky over a mackerel-cloud band): dawn, valley and sea clouds are tinted blue-white instead of warm peach/default white. Cloud sprites also ignore scene fog now — the warm dawn fog was washing the new tint out — and Mission 01 carries a denser, larger cloud band so the color actually reads.
- Sky color matched to the same reference photo: the dawn, valley and sea skies are now a vivid azure blue with a pale blue-white horizon haze, replacing the dark slate dawn and the paler day blues. Night and storm skies unchanged.
- Universal Cross-Device & Audio Craft Rule applied (now a standing rule for all games): adaptive graphics presets LOW/MED/HIGH in the pause banner — switchable mid-flight without resetting the run; LOW caps pixel ratio at 1, hides the sun glow/god rays and cuts particles ~70%, MED caps at 1.5 with ~40% fewer particles, HIGH is full quality; first load auto-picks MED on touch/small screens and HIGH on desktop, then remembers the choice. All audio now runs through a master bus with a SOUND ON/OFF toggle in the pause banner (remembered too), and explosions pan left/right with StereoPannerNode according to where they happen relative to the camera. Viewport now uses 100dvh + viewport-fit=cover; verified error-free at 1920×1080 desktop and 360×800 portrait. (Already in place and confirmed: dt clamped at 0.05 s, pooled particle systems, dual keyboard/mouse + touch input, AudioContext resume on first gesture.)

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
