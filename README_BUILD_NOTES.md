# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.22.2330

Focused UI and audio regression repair pass.

## Patch Intent

- Restore the newer cleaned-up HUD layout without rolling back recent Brasswake model/builder work.
- Move Captain's Orders back into the left panel so the selected-location panel and Fleet Log are easier to read.
- Restore the collapsible Command Menu with Save, Load, Help, Builder, Map, Reset, and music controls.
- Restore singleton music playback, mute, and volume persistence.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

## Issues Addressed

- The command controls and Captain's Orders had regressed into the lower HUD layout, crowding the Fleet Log and reducing selected-location readability.
- Music and volume controls were no longer present in the HUD.
- The active `index.html` no longer contained the music manager, volume persistence, or guarded music context hooks.

## Fixes Made

- Restored the left-column Captain's Orders panel and expanded bottom Fleet Log layout.
- Restored the collapsible lower-left Command Menu and kept the recent Fortress Builder button inside it.
- Restored the music on/off button, music volume slider, now-playing label, and unobtrusive debug line.
- Reintroduced a central singleton `MusicManager` using external MP3 paths under `assets/audio/music/`.
- Reconnected music context changes for title, campaign start, right-panel tabs, route plotting, travel, arrival, combat, result stingers, modal close, and load game.
- Preserved the latest Brasswake GLB layout and builder controls, including the saved underside engine ring and turn-engine placement.

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
- Checked version consistency for `v0.26.06.22.2330`.
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
