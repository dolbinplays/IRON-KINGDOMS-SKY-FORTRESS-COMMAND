# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.22.1900

Focused Brasswake Fortress Builder transform, undo, array, and variant pass.

## Patch Intent

- Make Brasswake module placement easier to tune by adding all-axis rotation controls.
- Add a bounded session-local undo stack for the most recent builder edits.
- Add circular array controls so repeated parts, especially underside engines, can be arranged around a slot center.
- Let locally loaded GLB variants be swapped per selected slot in the builder.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

## Issues Addressed

- The builder only exposed Y rotation, making it hard to correct GLB parts with different local orientations.
- Builder edits were immediate but had no undo path.
- Repeated underside parts had to be represented as separate slots rather than a quick circular array.
- Extra candidate GLBs in the selected model folder could not be previewed against an existing slot.

## Fixes Made

- Added RotX and RotZ sliders, numeric inputs, and nudge buttons while preserving RotY behavior.
- Added `Undo`, backed by a 25-entry session-local layout snapshot stack.
- Added circular array controls for selected slots: count 1-10, radius, start angle, angle span, vertical offset, and Face Outward.
- Array copies now render in both the live builder preview and the main Brasswake model using the same shared placement helper.
- Array copies use cloned cached GLB scenes or procedural fallbacks; clicking any copy in the preview selects the parent slot.
- Added variant support for locally selected GLB folders. Extra `.glb` files whose names start with a part's base filename appear in a Variant GLB selector for that slot.
- `Copy Layout` now exports full rotation arrays, optional `array` objects, and optional `variantFile` values.

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
- GLB files remain external under `assets/models/brasswake/`.

## Validation Performed

- Extracted JavaScript from `index.html` and ran syntax validation.
- Extracted module script from `index.html` and ran syntax validation.
- Checked inline `onclick` handlers for missing global function references.
- Checked duplicate function declarations.
- Checked version consistency for `v0.26.06.22.1900`.
- Confirmed Three.js CDN and matching module GLTFLoader references remain.
- Confirmed model paths point to `assets/models/brasswake/`.
- Confirmed all 15 Brasswake GLB files are present in the asset path.
- Confirmed referenced music files remain external and present.
- Confirmed no embedded audio/model data URLs.
- No embedded playable preview was created.

## Manual QA Still Recommended

- Open `index.html` directly in a browser, start/load a campaign, open Command -> Builder, click `Load GLB Folder`, and choose `assets/models/brasswake`.
- Test RotX, RotY, RotZ, and Scale on a visible slot.
- Set an underside engine slot to a circular array count between 2 and 10 and confirm copies appear in a ring.
- Toggle Face Outward and confirm the copies rotate around the ring.
- Use Undo after a transform, reset, array edit, and variant edit.
- If alternate GLBs are present in the folder, select them from Variant GLB and confirm the preview/main fortress swap models.
