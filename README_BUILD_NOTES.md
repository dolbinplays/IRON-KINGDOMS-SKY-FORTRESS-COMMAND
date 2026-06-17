# IRON KINGDOMS: SKY FORTRESS COMMAND

Version: v0.26.06.17.0200

## Patch Focus

Focused onboarding, readability, and roadmap-foundation patch based on the v0.26.06.17.0100 gameplay review.

## Major Changes

- Updated all visible/version/package/save metadata to v0.26.06.17.0200.
- Reworked Captain's Orders into an active Step 1-of-7 objective panel with compact progress dots.
- Locked the starting skyport's Local Contract until the player completes the first travel route, preventing the tutorial loop from being bypassed.
- Added local contract risk/reward preview before accepting contracts.
- Reduced repeated upgrade-available toast spam while preserving upgrade indicators in the command UI.
- Improved hex-board readability with brighter discovered tiles, stronger edges, reduced fog density, and clearer map contrast.
- Added a Map Focus toggle/button that hides command panels to show more of the hex board.
- Added Current Gate / Jet Stream Current route foundation:
  - Current Gate markers on routed locations.
  - Route network data stored in game state.
  - Safe, Trade, Storm, and Pirate route types.
  - Curved glowing current-route lines.
  - Route previews in selected-location panel.
  - Route-based travel costs layered over existing fallback direct travel.
- Added an eventful non-instant Jet Stream travel overlay with fantasy-steampunk storm-current flavor.
- Preserved existing systems: procedural hex map, travel, events, combat, rooms, upgrades, faction relations, AI events, autosave/manual save/load/reset, and Three.js CDN structure.

## Known Limitations

- Current Gates are an early route foundation and do not yet replace all direct travel.
- Jet Stream travel has a short overlay/progress treatment, not a full cinematic or interactive travel scene.
- Current route ownership, tolls, blockades, and hidden routes are not yet fully simulated.
- The Storm Keel / player-created temporary current engine is not implemented yet.
- Fortress rooms are still list/build-slot based, not the future fortress hex module builder.
- Combat remains panel-based rather than direct third-person fortress combat.
- Old saves from v0.26.06.17.0100 use a different save key and will not auto-load.

## Recommended Next Patch

Continue building the Current Gate system by adding deeper route logic: gate tolls, faction-controlled gates, route risk events, route locks, and a first Storm Keel research/unlock stub for temporary current creation.
