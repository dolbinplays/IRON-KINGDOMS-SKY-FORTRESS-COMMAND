IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.22.2330

Focused UI and audio regression repair pass.

PATCH INTENT
- Restore the newer cleaned-up HUD layout without rolling back recent Brasswake model/builder work.
- Move Captain's Orders back into the left panel so the selected-location panel and Fleet Log are easier to read.
- Restore the collapsible Command Menu with Save, Load, Help, Builder, Map, Reset, and music controls.
- Restore singleton music playback, mute, and volume persistence.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

ISSUES ADDRESSED
- The command controls and Captain's Orders had regressed into the lower HUD layout, crowding the Fleet Log and reducing selected-location readability.
- Music and volume controls were no longer present in the HUD.
- The active index.html no longer contained the music manager, volume persistence, or guarded music context hooks.

FIXES MADE
- Restored the left-column Captain's Orders panel and expanded bottom Fleet Log layout.
- Restored the collapsible lower-left Command Menu and kept the recent Fortress Builder button inside it.
- Restored the music on/off button, music volume slider, now-playing label, and unobtrusive debug line.
- Reintroduced a central singleton MusicManager using external MP3 paths under assets/audio/music/.
- Reconnected music context changes for title, campaign start, right-panel tabs, route plotting, travel, arrival, combat, result stingers, modal close, and load game.
- Preserved the latest Brasswake GLB layout and builder controls, including the saved underside engine ring and turn-engine placement.

MODEL FILES CHECKED
- Brasswake base platform.glb
- Brasswake command tower.glb
- Brasswake underside lift engine cluster.glb
- Brasswake underside turn engine cluster.glb
- Brasswake side docking arm.glb
- Brasswake small scout craft cradle.glb
- Brasswake expansion frame.glb
- Brasswake armor wall segment.glb
- Brasswake cannon turret.glb
- Brasswake radar mast.glb
- Brasswake hangar module.glb
- Brasswake foundry module.glb
- Brasswake storage module.glb
- Brasswake hydroponics module.glb
- Brasswake hospital module.glb

PRESERVED
- No early freeform direct travel.
- Current Gate / Jet Stream travel remains gate-locked.
- Clockwork Navigator / Celestial Navigation Automaton.
- Plot Capacity: 1 Jump.
- Captain's Orders onboarding.
- Current combat balance.
- Music singleton behavior.
- External MP3 assets under assets/audio/music/.
- External GLB assets under assets/models/brasswake/.

VALIDATION
- JavaScript extracted from index.html and syntax checked.
- Module script extracted from index.html and syntax checked.
- Inline onclick handlers checked for missing global functions.
- Duplicate function declarations checked.
- Version consistency checked for v0.26.06.22.2330.
- Three.js CDN and matching module GLTFLoader references checked.
- Model paths checked for assets/models/brasswake/.
- All 15 Brasswake GLB files confirmed in the asset path.
- Referenced music files remain external and present.
- No embedded audio/model data URLs found.
- No embedded playable preview created.

MANUAL QA STILL RECOMMENDED
- Open index.html directly in a browser, start/load a campaign, open Command -> Builder, click Load GLB Folder, and choose assets/models/brasswake.
- Test RotX, RotY, RotZ, and Scale on a visible slot.
- Set an underside engine slot to a circular array count between 2 and 10 and confirm copies appear in a ring.
- Toggle Face Outward and confirm the copies rotate around the ring.
- Use Undo after a transform, reset, array edit, and variant edit.
- If alternate GLBs are present in the folder, select them from Variant GLB and confirm the preview/main fortress swap models.
