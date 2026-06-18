# IRON KINGDOMS: SKY FORTRESS COMMAND v0.26.06.18.0900

Focused UI/map readability patch.

## Changes
- Updated all build/version/save labels to v0.26.06.18.0900.
- Improved zoomed-out map readability without removing the dark fantasy-steampunk mood.
- Reduced excessive distance fog and slightly lifted scene/background lighting.
- Increased hex tile visibility, route line readability, marker emissive strength, gate glow, and grid readability.
- Increased bottom HUD height and added safe side-panel bottom gutters so Command/Fleet/Orders no longer overlap Selected Location.
- Made Captain's Orders content scroll cleanly instead of clipping completed-orders suggestions.
- Preserved gate-locked travel, Current routes, Clockwork Navigator route planning, modular Brasswake marker, combat, salvage/harvest/trade/contracts/storm/ruin systems, upgrades/rooms/factions/tech tabs, and save/load behavior.

## Validation
- JavaScript syntax check passed with `node --check`.
- Version consistency check passed.
- ZIP integrity check passed.
- No GLB/GLTF loader added.
- No embedded preview generated.

## Known limitations
- This is a readability/layout patch only.
- It does not add new gameplay systems.
- It does not unlock Storm Keel route creation.
- It does not add tactical 3D mode or fortress builder.
- Browser playthrough was not run here to avoid embedded preview load.

## Recommended next patch
Run a short playtest of v0.26.06.18.0900. If the map and HUD are readable, the next patch should either:
- tie Brasswake visible modules to actual room/upgrade state, or
- continue route planner/Clockwork Navigator polish with better route path visualization and navigation upgrades.
