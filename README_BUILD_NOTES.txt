IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.23.0005

Focused Brasswake visual artifact cleanup pass.

PATCH INTENT
- Remove or hide unidentified camera/light/helper/icon-like artifacts that can appear inside the Brasswake nose/front area.
- Preserve real Brasswake GLB meshes, procedural fallback geometry, and Fortress Builder tools.
- Keep the game as a single-file HTML build using the existing Three.js CDN plus matching GLTFLoader module.
- Preserve external MP3 and GLB asset folders without base64 embedding.

ISSUES ADDRESSED
- Imported GLB scenes were cloned as whole scene graphs, so embedded cameras, lights, helper objects, debug nodes, or icon-like named meshes could be included in visible Brasswake assemblies.
- The procedural fallback includes intentional bow/nose lantern details that could be confused with imported helper artifacts during cleanup.
- Builder selection highlights needed to remain isolated to the Fortress Builder instead of being treated as normal gameplay geometry.

FIXES MADE
- Added sanitizeImportedBrasswakePart() to strip imported cameras, lights, helper classes, debug/icon nodes, and strictly named helper/icon meshes before a GLB part is normalized and placed.
- Kept real part meshes conservative by only removing mesh objects whose names clearly indicate helper/debug/icon artifacts.
- Marked intentional procedural bow/nose lanterns as Brasswake decoration so they remain available as fallback visual details.
- Preserved the existing GLB cache/clone flow, builder preview, circular arrays, variants, turn-then-move travel facing, and procedural fallbacks.

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
- Selected Location UI and Command Menu layout.
- Current combat balance.
- Music singleton behavior and restored audio controls.
- Brasswake GLB module visuals, Fortress Builder, live preview, arrays, variants, and Copy Layout.
- External MP3 assets under assets/audio/music/.
- External GLB assets under assets/models/brasswake/.

VALIDATION
- JavaScript extracted from index.html and syntax checked.
- Module script extracted from index.html and syntax checked.
- Inline onclick handlers checked for missing global functions.
- Duplicate function declarations checked.
- Version consistency checked for v0.26.06.23.0005.
- Three.js CDN and matching module GLTFLoader references checked.
- Model paths checked for assets/models/brasswake/.
- All 15 Brasswake GLB files confirmed in the asset path.
- Referenced music files remain external and present.
- No embedded audio/model data URLs found.
- No embedded playable preview created.

MANUAL QA STILL RECOMMENDED
- Open index.html directly in a browser and start or load a campaign.
- Confirm the unidentified nose/front artifact no longer appears on the main Brasswake model.
- Open Command -> Builder, click Load GLB Folder, choose assets/models/brasswake, and confirm the builder preview also omits the artifact.
- Confirm intentional bow/nose lantern fallback details are acceptable; if they are the visible issue, they can be tuned or removed in a follow-up visual pass.
