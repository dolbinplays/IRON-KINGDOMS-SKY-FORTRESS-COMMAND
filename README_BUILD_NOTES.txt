IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.23.0006

Focused V3 Inherited Craft Foundation patch.

PATCH INTENT
- Reframe the campaign start around the inherited Tier 0 skiff Brass Minnow.
- Add explicit active craft data through playerShip, activeShipId, and ownedShips.
- Keep Brasswake locked as a future modular flying fortress-city milestone.
- Preserve the current single-file HTML / JavaScript / Three.js CDN prototype.

CHANGES MADE
- Added starter ship data for Brass Minnow, including class, tier, crew berths, cargo capacity, ratings, and Clockwork Navigator details.
- Added locked brasswake milestone state and future Brasswake Free Command faction state.
- Repurposed the left status panel from fortress framing to Ship Status.
- Updated title screen, opening log, Captain's Orders, roadmap doctrine, selected-location nudges, travel text, and combat labels to support the inherited-craft start.
- Reframed active upgrades as craft refits while preserving the existing module prototype for testing.

SAVE COMPATIBILITY
- SAVE_KEY was bumped to IK_SKY_FORTRESS_COMMAND_v0_26_06_23_0006.
- The bump is intentional because root save data now includes ship progression, Brasswake milestone, and future faction fields.
- Load normalization also fills missing V3 fields if compatible data is encountered.

PRESERVED
- Current Gate / Jet Stream route plotting.
- Turn-then-move directional travel facing.
- Procedural hex-board layout.
- Captain's Orders panel layout.
- Collapsible Command Menu.
- Expanded Fleet Log.
- Selected Location panel.
- Contracts, salvage, harvest, trade, enemies, depleted states, route events, autosave, manual save, reset.
- Singleton MusicManager and existing external MP3 asset flow.
- Existing Brasswake GLB/model/builder internals as prototype systems.

VALIDATION
- JavaScript syntax check.
- Module script syntax check.
- Version and save key consistency check.
- Route/facing function inspection confirmed no movement rewrite.
- Package structure checked.
- No embedded playable preview was created.

MANUAL QA STILL RECOMMENDED
- Open index.html directly in a browser.
- Start a new campaign and confirm the title/opening log/Ship Status show Brass Minnow.
- Select a nearby node and confirm route preview still works.
- Travel through a Current Gate / Jet Stream and confirm the craft turns toward the next hop and preserves facing after arrival.
- Confirm contracts, salvage, harvest, trade, repair/refuel, save/load/reset, and music controls still work.
