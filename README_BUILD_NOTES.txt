IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.22.2006

Focused Brasswake tuned layout and underside lift engine array pass.

PATCH INTENT
- Apply the user's copied Brasswake Builder layout as the new source layout.
- Add a six-engine circular array to the underside lift engine slot so the ring is visible by default.
- Preserve the builder's all-axis rotation, undo, circular array, variant, and live preview controls.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

ISSUES ADDRESSED
- The copied layout did not include an array object for undersideLift, so the game/export still represented that slot as one engine.
- The tuned module placements needed to be made permanent in BRASSWAKE_SLOT_LAYOUT.

FIXES MADE
- Replaced the default slot table with the user's copied layout values.
- Added array: count 6, radius 1.05, startAngle 0.00, angleSpan 6.28, yOffset 0.00, faceOutward true to undersideLift.
- Kept the shared array placement helper so the six lift engines render in both the main fortress and builder preview.

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
- Version consistency checked for v0.26.06.22.2006.
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
