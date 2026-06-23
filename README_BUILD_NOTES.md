# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.22.2352

Focused Selected Location readability and early-action guidance pass.

## Patch Intent

- Use the lower-left space recovered by the collapsible Command Menu to expand the Selected Location panel.
- Make selected-location actions and travel buttons visible earlier in the panel.
- Add roadmap-aligned first-session and post-arrival guidance so players know what to do next after selecting or reaching a location.
- Preserve the restored Command Menu, audio controls, Brasswake model/builder work, and current travel rules.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

## Issues Addressed

- The left panel still stopped above the Fleet Log even though command controls had moved into a collapsible lower-left dock.
- Selected-location route/details could push the actual action buttons down the panel.
- Arrival feedback was readable but did not always tell the player which local action to take next.
- Battle music could remain selected after combat resolution, making non-combat tiles continue to use combat music.
- Victory stingers could be missed because combat result audio was requested before combat state fully cleared.

## Fixes Made

- Extended the left HUD column down to the Command Menu button, giving Selected Location more vertical room.
- Added a compact Recommended Next cue to the selected-location panel.
- Moved selected-location action buttons above route previews, navigator summaries, and secondary detail blocks.
- Added selected-action styling so primary travel/local actions are easier to scan.
- Added clearer post-arrival toasts for salvage, resource, storm, enemy, ruin, contract, and service-port locations.
- Adjusted combat result music ordering so combat state clears before contextual music restore and victory/retreat/defeat stingers.
- Preserved the restored Command Menu/audio controls and the latest Brasswake GLB layout/builder systems.

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
- Checked version consistency for `v0.26.06.22.2352`.
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
