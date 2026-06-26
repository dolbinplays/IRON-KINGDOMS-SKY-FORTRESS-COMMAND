IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.26.0001

Focused Brass Minnow starter craft visual patch.

#Patch Intent

- Replace the older fortress-style active craft marker with a small starter-skiff visual.
- Make Brass Minnow read as a tiny inherited courier/utility craft from the strategy camera.
- Keep the model deliberately simple and placeholder-friendly.
- Preserve all route, action, save, music, and V3 progression systems.

#Changes Made

- Updated version labels, title, VERSION, README/build notes, package folder, ZIP naming, and manifest to v0.26.06.26.0001.
- Kept SAVE_KEY at IK_SKY_FORTRESS_COMMAND_v0_26_06_24_0001 because this is a visual/model patch and should preserve existing test saves.
- Added createBrassMinnowModel() as the active player craft factory.
- Added modular helper functions for Minnow materials, main hull, rear engine block, left/right lift pods, tail assembly, top deck/cargo plate, small utility arm, and patch plates.
- Replaced startup active craft creation with the Brass Minnow skiff model.
- Added a guard so Brasswake model refreshes do not attach fortress modules to the active starter craft.
- Preserved legacy/future Brasswake GLB/procedural tooling for later fortress-city milestones.
- Updated travel modal wording to refer to the active craft instead of the fortress.
- Updated in-game build notes to describe the skiff visual and save-key decision.

#Systems Intentionally Preserved

- Single-file HTML structure.
- Existing Three.js CDN and GLTFLoader approach.
- Three.js overworld rendering and GLB/model support.
- Procedural hex-board layout.
- Current Gate / Jet Stream route plotting.
- Multi-hop route planner and No Charted Current messaging.
- Turn-then-move directional travel facing.
- Captain's Orders panel.
- Ship Status panel.
- Selected Location panel and route/action button generation.
- Collapsible Command Menu.
- Fleet Log scrolling behavior.
- Existing contracts, salvage, harvest, trade, combat, route events, and depleted states.
- Fuel, food, steel, gold, and internal population/support behavior.
- Autosave, manual save, load, and reset.
- Singleton MusicManager and external MP3 asset flow.
- Storm Keel, Saint Elmo Navigation Core, and Astrolabe Engine locks.

#Validation Performed

- Version string check by inspection/counts.
- Active craft startup path check: startup now calls createBrassMinnowModel().
- Brasswake refresh guard check: active Brass Minnow groups are skipped.
- Duplicate showBuildNotes() check.
- Save-key decision checked: unchanged intentionally for compatibility.
- Route/facing function preservation check by inspection.
- Music manager inspection confirmed no second manager was added.
- Package structure checked.
- JavaScript execution/syntax checks could not be run because Node is not available on PATH in this shell.
- No embedded playable preview was created.

#Manual QA Still Recommended

- Open index.html directly in a browser.
- Start a new campaign and confirm the active craft reads as a small skiff, not a fortress.
- Load the existing save and confirm Ship Status still shows Brass Minnow details.
- Rotate/observe the map enough to confirm the bow, rear engine block, side lift pods, tail fin, and deck/cargo plate are readable.
- Plot and ride a Current Gate / Jet Stream route and confirm the craft turns before travel and preserves facing after arrival.
- Confirm Selected Location, Captain's Orders, Fleet Log, contracts, salvage, harvest, trade, music, save/load, and reset still work.