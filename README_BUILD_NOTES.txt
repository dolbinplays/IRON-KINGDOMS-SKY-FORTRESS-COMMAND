IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.24.0003

Focused left HUD hierarchy cleanup patch.

#Patch Intent

- Make Selected Location feel more important than Ship Status.
- Keep the active craft readable at a glance without letting ship metadata crowd out available actions.
- Preserve all route, action, save, music, and V3 progression systems.

#Changes Made

- Updated version labels, title, VERSION, README/build notes, package folder, ZIP naming, and manifest to v0.26.06.24.0003.
- Kept SAVE_KEY at IK_SKY_FORTRESS_COMMAND_v0_26_06_24_0001 because this is a layout-only patch and should preserve existing test saves.
- Reordered the left HUD to place Selected Location directly below compact Ship Status and above Captain's Orders.
- Changed Ship Status to default to only craft name and hull health.
- Moved tier, class, crew, cargo, navigator, plot capacity, Brasswake milestone text, and Support clarification behind an expandable Craft Details section.
- Increased the Selected Location panel minimum height so available buttons and route/action context have more room.
- Reduced the Captain's Orders maximum height so it remains useful without competing for the main interaction space.
- Updated in-game build notes to describe the hierarchy change and save-key decision.

#Systems Intentionally Preserved

- Single-file HTML structure.
- Existing Three.js CDN and GLTFLoader approach.
- Three.js overworld rendering and GLB/model support.
- Procedural hex-board layout.
- Current Gate / Jet Stream route plotting.
- Multi-hop route planner and No Charted Current messaging.
- Turn-then-move directional travel facing.
- Captain's Orders logic.
- Collapsible Command Menu.
- Fleet Log scrolling behavior.
- Selected Location actions and route/action button generation.
- Existing contracts, salvage, harvest, trade, combat, route events, and depleted states.
- Fuel, food, steel, gold, and internal population/support behavior.
- Autosave, manual save, load, and reset.
- Singleton MusicManager and external MP3 asset flow.
- Storm Keel, Saint Elmo Navigation Core, and Astrolabe Engine locks.

#Validation Performed

- Version string check by inspection/counts.
- Duplicate showBuildNotes() check.
- Save-key decision checked: unchanged intentionally for compatibility.
- Route/facing function preservation check by inspection.
- Music manager inspection confirmed no second manager was added.
- Package structure checked.
- JavaScript execution/syntax checks could not be run because Node is not available on PATH in this shell.
- No embedded playable preview was created.

#Manual QA Still Recommended

- Open index.html directly in a browser.
- Load the existing save and confirm Ship Status shows only Brass Minnow and hull by default.
- Expand Craft Details and confirm tier, class, crew, cargo, navigator, plot capacity, and Support clarification are still available.
- Select a nearby location and confirm travel/action buttons are visible higher in the Selected Location panel.
- Confirm Captain's Orders still scrolls/renders and remains readable below Selected Location.
- Plot and ride a Current Gate / Jet Stream route and confirm facing behavior is preserved.
- Confirm save/load/reset and music controls still work.