# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.22.2325

Focused Brasswake underside engine layout refinement pass.

## Patch Intent

- Apply the user's saved Brasswake Builder underside engine refinements.
- Tune the six-engine underside lift ring scale and facing.
- Move and rotate the underside turn engine cluster into its revised aft-side placement.
- Preserve the builder's all-axis rotation, undo, circular array, variant, and live preview controls.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

## Issues Addressed

- The previous committed lift engine ring was too large and faced outward; the saved layout uses smaller engines without outward yawing.
- The underside turn engine cluster needed the latest saved placement, all-axis rotation, and scale.

## Fixes Made

- Updated `undersideLift` to `scale: 0.47` and `faceOutward: false` while keeping the six-engine ring.
- Updated `undersideTurn` to position `[2.80, -0.10, -0.10]`, rotation `[-1.60, 0.45, 1.60]`, and scale `0.80`.
- Kept the shared array placement helper so the six lift engines render in both the main fortress and builder preview.

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
- Checked version consistency for `v0.26.06.22.2325`.
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
