# IRON KINGDOMS: SKY FORTRESS COMMAND v0.26.06.17.0800

## Patch Summary

This focused patch upgrades Brasswake's overworld marker from a simple airship placeholder into a lightweight procedural modular hex-built sky fortress model using only built-in Three.js geometry.

## Brasswake Model Changes

- Replaced `createFortressModel()` with a procedural modular hex fortress marker.
- Added a raised central command/bridge hex with warm window glow and signal mast.
- Added outer functional hex modules: engine/workshop, boiler, cannon decks, storage, barracks, dock platform, and an empty future expansion frame.
- Added underside blue-white arc-lift rings, small lift pods, a central lift assembly, pipes, catwalks, support braces, cables/chains, smokestacks, cannons, rivets, patch plates, vents, railings, crane detail, and warm lantern/window glow.
- Added subtle arc-lift pulse/rotation while preserving the current fortress bobbing behavior.

## Preserved Systems

- Single-file HTML structure.
- Three.js CDN usage.
- Existing overworld, hex board, Current Gate network, gate-locked strategic travel, multi-hop route planner, Clockwork Navigator / Celestial Navigation Automaton systems, Tech tab, Storm Keel locked state, combat, salvage, contracts, rooms/upgrades/factions, save/load/autosave, and all existing UI flows.

## Known Limitations

- This is still a lightweight in-map representation, not the final fortress-builder system.
- Visible modules are not yet mechanically tied to actual rooms/upgrades.
- No GLB asset is loaded yet; the model remains procedural to keep the game single-file and stable.
- Storm Keel temporary current generation remains locked for future progression.

## Recommended Next Patch

Tie visible Brasswake modules to room/upgrade state in a controlled way: installed rooms could subtly light or add detail to matching hex modules, while future rooms could fill empty expansion frames.
