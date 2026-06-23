# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.22.1833

Focused Brasswake visual builder usability and direct-file GLB loading pass.

## Patch Intent

- Make the loaded Brasswake GLB assembly read as one cohesive modular flying fortress-city.
- Preserve the restored turn-in-place-before-moving fortress travel behavior.
- Add a more visual in-game Fortress Builder so slot placement can be tuned against a live preview instead of guessed.
- Make the real GLB files easier to load when opening `index.html` directly from disk.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

## Issues Addressed

- The GLBs were loading, but the fortress could read as small disconnected model parts rather than a unified player fortress.
- The forward direction was still hard to read in motion because the model did not have a strong bow cue.
- Iterating GLB slot placement required code-only edits and browser reloads, slowing technical-art tuning.
- When opened directly as a `file://` page, browser security can block `GLTFLoader` from fetching external GLB files by relative path, leaving only procedural fallback primitives visible.

## Fixes Made

- Added a larger shared foundation hull under the GLB assembly so Brasswake has a continuous fortress silhouette.
- Added a bright bow prow and lantern at local negative X, matching the rule that the left-pointing side is the front of Brasswake.
- Increased the overall fortress root scale and tightened the starting GLB slot layout.
- Expanded the Builder into a three-column layout with a visual slot list, a dedicated live Three.js fortress preview, and transform controls.
- The Builder can select slots, preview locked future modules, click parts in the preview, orbit/zoom the preview, nudge position, adjust Y rotation and scale with sliders plus numeric inputs, snap to deck height, center on hull, reset one slot or all slots, and copy the current `BRASSWAKE_SLOT_LAYOUT` table.
- Added a `Load GLB Folder` action for direct-file testing. Choose `assets/models/brasswake` so the browser can use local `.glb` object URLs instead of blocked `file://` fetches.
- Kept the GLTFLoader module path, cached GLB cloning, per-slot fallback meshes, and persistent `game.fortressFacing` travel behavior intact.

## Model Files Checked

All 15 model files are expected under `assets/models/brasswake/`:

- `Brasswake base platform.glb`
- `Brasswake command tower.glb`
- `Brasswake underside lift engine cluster.glb`
- `Brasswake underside turn engine cluster.glb`
- `Brasswake side docking arm.glb`
- `Brasswake small scout craft cradle.glb`
- `Brasswake expansion frame.glb`
- `Brasswake armor wall segment.glb`
- `Brasswake cannon turret.glb`
- `Brasswake radar mast.glb`
- `Brasswake hangar module.glb`
- `Brasswake foundry module.glb`
- `Brasswake storage module.glb`
- `Brasswake hydroponics module.glb`
- `Brasswake hospital module.glb`

## Systems Intentionally Preserved

- No early freeform direct travel was restored.
- Current Gate / Jet Stream travel remains gate-locked.
- Clockwork Navigator / Celestial Navigation Automaton remains preserved.
- Plot Capacity remains 1 Jump.
- Captain's Orders onboarding remains preserved.
- Combat balance was not changed.
- Music singleton behavior was not changed.
- MP3 files remain external under `assets/audio/music/`.

## Validation Performed

- Extracted JavaScript from `index.html` and ran syntax validation.
- Extracted module script from `index.html` and ran syntax validation.
- Checked inline `onclick` handlers for missing global function references.
- Checked duplicate function declarations.
- Checked version consistency for `v0.26.06.22.1833`.
- Confirmed Three.js CDN and matching module GLTFLoader references remain.
- Confirmed model paths point to `assets/models/brasswake/`.
- Confirmed all 15 Brasswake GLB files are present in the asset path.
- Confirmed the local GLB folder loader does not base64-embed model assets.
- Confirmed referenced music files remain external.
- Confirmed no embedded audio/model data URLs.
- No embedded playable preview was created.

## Manual QA Still Recommended

- Open `index.html` directly in a browser, start/load a campaign, open Command -> Builder, click `Load GLB Folder`, and choose `assets/models/brasswake`.
- Confirm the builder status reports local GLBs active and the preview/main fortress replace fallback primitives with real parts.
- Use the live preview to orbit, click a slot, nudge it with sliders, confirm the highlight updates immediately, then reset the slot.
- Ride a Current Gate / Jet Stream hop and confirm Brasswake turns before moving, then remains facing the arrival direction.
