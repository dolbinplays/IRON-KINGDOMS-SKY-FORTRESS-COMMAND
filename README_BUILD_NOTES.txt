IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.24.0001

Focused V3 cleanup and roadmap foundation patch.

PATCH INTENT
- Fix the leftover IRON KINGDOMS: WAR OF BRASS title-screen kicker.
- Keep the campaign start centered on Brass Minnow, an Inherited Courier Skiff and Tier 0 - Inherited Craft.
- Keep Brasswake locked as a future modular flying fortress-city milestone.
- Clarify prototype-wide Support versus active skiff crew.
- Add the first lightweight foundation for V3 reputation and career-tagged contracts.

CHANGES MADE
- Updated version labels, title, VERSION, SAVE_KEY, manifest, README/build notes, package folder, and ZIP naming to v0.26.06.24.0001.
- Changed the title-screen kicker to IRON KINGDOMS: SKY FORTRESS COMMAND.
- Changed the visible top-bar population label to Support while preserving the internal resources.population key.
- Added Ship Status explanatory text: Support is prototype-wide capacity; active skiff crew is shown as playerShip.crewUsed / playerShip.crewCapacity.
- Consolidated duplicate showBuildNotes() logic into one authoritative function.
- Added V3 reputation state with Duke, Merchant, Explorer, Military, Freebooter, and per-kingdom reputation tracks.
- Added reputation tier helpers and a compact Reputation Summary to the Factions tab.
- Added career-style contract tags and displayed them in selected-location details and settlement contract previews.
- Added small Fleet Log reputation rewards to existing salvage, resource, contract, trade, repair, exploration, settlement-contract, and combat outcomes.

SAVE COMPATIBILITY
- SAVE_KEY was bumped to IK_SKY_FORTRESS_COMMAND_v0_26_06_24_0001.
- The bump is intentional because the campaign root now includes new V3 reputation and contract/career roadmap foundation state.
- Load normalization also ensures V3 ship, milestone, faction, and reputation fields exist if compatible state is loaded.

PRESERVED
- Single-file HTML structure.
- Existing Three.js CDN and GLTFLoader approach.
- Three.js overworld rendering and GLB/model support.
- Procedural hex-board layout.
- Current Gate / Jet Stream route plotting.
- Multi-hop route planner and No Charted Current messaging.
- Turn-then-move directional travel facing.
- Captain's Orders panel.
- Collapsible Command Menu.
- Expanded Fleet Log.
- Selected Location panel.
- Existing contracts, salvage, harvest, trade, combat, route events, and depleted states.
- Fuel, food, steel, gold, and internal population/support behavior.
- Autosave, manual save, load, and reset.
- Singleton MusicManager and external MP3 asset flow.
- Storm Keel, Saint Elmo Navigation Core, and Astrolabe Engine locks.

VALIDATION
- JavaScript syntax check.
- Module wrapper syntax check.
- Inline handler/global function check.
- Duplicate showBuildNotes() check.
- Version and save-key consistency check.
- Route/facing function inspection confirmed no movement rewrite.
- Music manager inspection confirmed no second manager was added.
- Package structure checked.
- No embedded playable preview was created.

MANUAL QA STILL RECOMMENDED
- Open index.html directly in a browser.
- Confirm the title screen says IRON KINGDOMS: SKY FORTRESS COMMAND.
- Start a new campaign and confirm Ship Status shows Brass Minnow, Inherited Courier Skiff, and Tier 0 - Inherited Craft.
- Confirm the top resource bar says Support, not fortress-sized crew.
- Open the Factions tab and confirm Reputation Summary renders.
- Select contract/salvage/resource/combat locations and confirm tags display.
- Complete a salvage or contract action and confirm a Fleet Log reputation line appears.
- Plot and ride a Current Gate / Jet Stream route and confirm facing behavior is preserved.
- Confirm save/load/reset and music controls still work.
