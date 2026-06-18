# IRON KINGDOMS: SKY FORTRESS COMMAND — v0.26.06.18.1000

Focused HUD polish patch.

## Changes

- Converts completed Captain's Orders into a compact Captain's Wings earned panel.
- Shows a brass/gold CSS-only Open Command wings badge after the short tutorial is complete.
- Adds a simple temporary HUD alert overlay in the Captain's Wings area after tutorial completion.
- Keeps the wings faintly visible behind alerts so the space can become a future command/status area.
- Replaces long permanent Open Command bullet lists with one compact suggestion.
- Fixes Selected Location scroll-bottom clipping by making the Selected Location panel a dedicated flex scroller.
- Adds bottom padding and a safe scroll gutter so final notes/buttons are visible at full scroll.

## Preserved

- Single-file HTML structure.
- Three.js CDN usage.
- Current overworld, hex board, route network, travel, combat, rooms, upgrades, factions, tech, save/load/autosave.
- Gate-locked early strategic travel.
- Storm Keel remains locked.
- No GLB/GLTF loader.
- No embedded preview.

## Known Limitations

- This is a focused HUD polish patch only.
- The HUD alert overlay is intentionally simple and not a full alert queue system yet.
- Captain's Wings are CSS-only and can be upgraded with custom art later.
- Future work can expand this area into a richer command notification/status system.

## Validation

- JavaScript syntax check passed with `node --check`.
- Version references updated to v0.26.06.18.1000.
- Save key updated to `IK_SKY_FORTRESS_COMMAND_v0_26_06_18_1000`.
