IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.22.1900

Focused Brasswake Fortress Builder transform, undo, array, and variant pass.

PATCH INTENT
- Make Brasswake module placement easier to tune by adding all-axis rotation controls.
- Add a bounded session-local undo stack for the most recent builder edits.
- Add circular array controls so repeated parts, especially underside engines, can be arranged around a slot center.
- Let locally loaded GLB variants be swapped per selected slot in the builder.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

ISSUES ADDRESSED
- The builder only exposed Y rotation, making it hard to correct GLB parts with different local orientations.
- Builder edits were immediate but had no undo path.
- Repeated underside parts had to be represented as separate slots rather than a quick circular array.
- Extra candidate GLBs in the selected model folder could not be previewed against an existing slot.

FIXES MADE
- Added RotX and RotZ sliders, numeric inputs, and nudge buttons while preserving RotY behavior.
- Added Undo, backed by a 25-entry session-local layout snapshot stack.
- Added circular array controls for selected slots: count 1-10, radius, start angle, angle span, vertical offset, and Face Outward.
- Array copies now render in both the live builder preview and the main Brasswake model using the same shared placement helper.
- Array copies use cloned cached GLB scenes or procedural fallbacks; clicking any copy in the preview selects the parent slot.
- Added variant support for locally selected GLB folders. Extra .glb files whose names start with a part's base filename appear in a Variant GLB selector for that slot.
- Copy Layout now exports full rotation arrays, optional array objects, and optional variantFile values.

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
- Version consistency checked for v0.26.06.22.1900.
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
