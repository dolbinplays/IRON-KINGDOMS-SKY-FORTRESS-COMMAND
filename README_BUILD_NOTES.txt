IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.22.2325

Focused Brasswake underside engine layout refinement pass.

PATCH INTENT
- Apply the user's saved Brasswake Builder underside engine refinements.
- Tune the six-engine underside lift ring scale and facing.
- Move and rotate the underside turn engine cluster into its revised aft-side placement.
- Preserve the builder's all-axis rotation, undo, circular array, variant, and live preview controls.
- Preserve GLB fallbacks, save/load compatibility, gate-locked Current Gate travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, combat balance, and singleton music behavior.

ISSUES ADDRESSED
- The previous committed lift engine ring was too large and faced outward; the saved layout uses smaller engines without outward yawing.
- The underside turn engine cluster needed the latest saved placement, all-axis rotation, and scale.

FIXES MADE
- Updated undersideLift to scale 0.47 and faceOutward false while keeping the six-engine ring.
- Updated undersideTurn to position [2.80, -0.10, -0.10], rotation [-1.60, 0.45, 1.60], and scale 0.80.
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
- Version consistency checked for v0.26.06.22.2325.
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
