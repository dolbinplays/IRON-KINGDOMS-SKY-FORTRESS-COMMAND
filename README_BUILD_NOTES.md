# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.23.0005

Focused Brasswake visual artifact cleanup pass.

## Patch Intent

- Remove or hide unidentified camera/light/helper/icon-like artifacts that can appear inside the Brasswake nose/front area.
- Preserve real Brasswake GLB meshes, procedural fallback geometry, and Fortress Builder tools.
- Keep the game as a single-file HTML build using the existing Three.js CDN plus matching GLTFLoader module.
- Preserve external MP3 and GLB asset folders without base64 embedding.

## Issues Addressed

- Imported GLB scenes were cloned as whole scene graphs, so embedded cameras, lights, helper objects, debug nodes, or icon-like named meshes could be included in visible Brasswake assemblies.
- The procedural fallback includes intentional bow/nose lantern details that could be confused with imported helper artifacts during cleanup.
- Builder selection highlights needed to remain isolated to the Fortress Builder instead of being treated as normal gameplay geometry.

## Fixes Made

- Added `sanitizeImportedBrasswakePart()` to strip imported cameras, lights, helper classes, debug/icon nodes, and strictly named helper/icon meshes before a GLB part is normalized and placed.
- Kept real part meshes conservative by only removing mesh objects whose names clearly indicate helper/debug/icon artifacts.
- Marked intentional procedural bow/nose lanterns as Brasswake decoration so they remain available as fallback visual details.
- Preserved the existing GLB cache/clone flow, builder preview, circular arrays, variants, turn-then-move travel facing, and procedural fallbacks.

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
- Selected Location UI and Command Menu layout remain preserved.
- Combat balance was not changed.
- Music singleton behavior and restored audio controls were not changed.
- Brasswake GLB module visuals, Fortress Builder, live preview, arrays, variants, and Copy Layout remain preserved.
- MP3 files remain external under `assets/audio/music/`.
- GLB files remain external under `assets/models/brasswake/`.

## Validation Performed

- Extracted JavaScript from `index.html` and ran syntax validation.
- Extracted module script from `index.html` and ran syntax validation.
- Checked inline `onclick` handlers for missing global function references.
- Checked duplicate function declarations.
- Checked version consistency for `v0.26.06.23.0005`.
- Confirmed Three.js CDN and matching module GLTFLoader references remain.
- Confirmed model paths point to `assets/models/brasswake/`.
- Confirmed all 15 Brasswake GLB files are present in the asset path.
- Confirmed referenced music files remain external and present.
- Confirmed no embedded audio/model data URLs.
- No embedded playable preview was created.

## Manual QA Still Recommended

- Open `index.html` directly in a browser and start or load a campaign.
- Confirm the unidentified nose/front artifact no longer appears on the main Brasswake model.
- Open Command -> Builder, click `Load GLB Folder`, choose `assets/models/brasswake`, and confirm the builder preview also omits the artifact.
- Confirm intentional bow/nose lantern fallback details are acceptable; if they are the visible issue, they can be tuned or removed in a follow-up visual pass.
