# IRON KINGDOMS: SKY FORTRESS COMMAND — v0.26.06.17.0400

Focused tutorial-completion, direct-travel polish, faction-gate roadmap patch.

## Changed

- Updated displayed build label, VERSION constant, SAVE_KEY, standalone filename, package folder, and build notes to v0.26.06.17.0400.
- Added proper Captain's Orders completion state and Open Command suggestions after 7/7 tutorial objectives.
- Delayed early upgrade nudges so they no longer compete with the first travel tutorial.
- Added direct engine travel confirmation for medium/long, costly, risky, or low-hull direct routes.
- Added low-hull direct-travel warnings.
- Added faction-controlled gate policy foundation: owner, standing, toll, permit/inspection risk, blockade risk, event risk.
- Added route toll handling and fallback messaging if a toll cannot be afforded.
- Expanded route events with faction-flavored outcomes.
- Improved enemy fleet naming by faction.
- Added compact route legend to the selected-location panel.
- Fixed the hex mesh orientation to match the pointy-top axial hex coordinate math, eliminating the large triangular gaps between tiles.

## Known Limitations

- Current Gates are still a foundation layer, not the full final route-network diplomacy system.
- Blockades/permits are warning-and-event based; they do not yet create full strategic locks or negotiation flows.
- Direct travel still exists as a prototype fallback.
- Storm Keel temporary-current creation is not implemented yet.
- Fortress hex module building is not implemented yet.
- Tactical 3rd-person fortress flight is not implemented yet.
- Older saves use previous version save keys and will not auto-load.

## Recommended Next Patch

Continue with either Storm Keel / temporary current unlock foundation, deeper gate diplomacy, richer route events, or the first fortress hex module builder foundation.
