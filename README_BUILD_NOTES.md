# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.20.1245

Focused directional fortress travel patch.

## Patch Intent

- Make Brasswake visually face the direction of each Current Gate / Jet Stream jump.
- Treat the left-pointing segment of the current procedural fortress model as the bow/front.
- Preserve gate-locked travel, Clockwork Navigator rules, Plot Capacity: 1 Jump, Captain's Orders, singleton music, combat balance, and the single-file HTML build.

## Issues Addressed

- Brasswake could slide from one hex to another without first facing the destination, making travel feel less intentional.
- The render loop applied a decorative yaw sway every frame, which would prevent a persistent travel heading from surviving map rebuilds, autosaves, arrivals, or reloads.
- Older saves had no stored fortress-facing field.

## Fixes Made

- Added persistent `game.fortressFacing` state with a safe default for new and loaded campaigns.
- Added angle normalization and shortest-turn helpers for stable Three.js Y rotation.
- Added destination-facing math that treats the model's local/world `-X` direction as the bow.
- Updated travel animation to rotate in place first, then move along the current jump.
- Updated map rebuild/position refresh to restore the saved fortress facing.
- Removed the old idle yaw override so Brasswake remains pointed in its last travel direction after arrival.

## Systems Intentionally Preserved

- No early freeform direct travel was restored.
- Gate-locked Current Gate / Jet Stream travel remains the primary travel method.
- Clockwork Navigator / Celestial Navigation Automaton remains installed at campaign start.
- Plot Capacity remains 1 Jump.
- Captain's Orders and Open Command are preserved.
- Combat balance was not changed.
- Music behavior was not changed; loop music remains singleton-managed and MP3 assets remain external under `assets/audio/music/`.
- The build remains a single-file HTML game using the Three.js CDN.

## Validation Performed

- Extracted JavaScript from `index.html` and ran syntax validation.
- Checked inline `onclick` handlers for missing global function references.
- Checked version strings for `v0.26.06.20.1245`.
- Confirmed Three.js CDN reference remains.
- Confirmed music paths remain relative under `assets/audio/music/`.
- Confirmed referenced music files exist.
- Confirmed no embedded audio data URLs.
- No embedded playable preview was created.

## Deferred

- No route-rule changes, combat balance changes, music-system changes, or fortress model redesigns were attempted.
- Live browser/game-feel verification should still be done by riding a one-hop Current and then a continued plotted route.
