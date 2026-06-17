IRON KINGDOMS: SKY FORTRESS COMMAND — v0.26.06.17.0600

Focused gate-locked route planning, tutorial guidance, and Storm Keel visibility patch.

Package contents:
- index.html — single-file browser build using Three.js CDN
- README_BUILD_NOTES.txt — this file

Version consistency:
- Displayed version label: v0.26.06.17.0600
- VERSION constant: v0.26.06.17.0600
- Save key metadata: IK_SKY_FORTRESS_COMMAND_v0_26_06_17_0600
- Package/folder name: IRON_KINGDOMS_SKY_FORTRESS_COMMAND_v0.26.06.17.0600

Summary of changes:
- Added first multi-hop Current Gate route planner using the existing route graph.
- Destinations without direct Current routes can now show reachable multi-hop paths, next hop, total fuel, total days, tolls, highest risk, and route path text.
- Added Plot Route / Select Next Hop behavior instead of restoring direct overworld travel.
- Improved No Charted Current messaging for truly unreachable destinations.
- Added route visual hierarchy: current-adjacent routes are brighter, selected/plotted paths are highlighted, unrelated routes are dimmer.
- Added map/tooltip feedback for direct, multi-hop reachable, and unreachable Current destinations.
- Added combat tutorial guidance that can plot a route to the nearest reachable Danger 1 enemy.
- Hardened selected-location panel scroll reset after selection, travel, events, and modal close.
- Added a Tech tab and made Storm Keel more visible as locked mid/late travel technology.
- Added Storm Keel Core as a future-content requirement so Storm Keel remains a major later milestone.
- Tuned upgrade panel emphasis to recommend one upgrade instead of making every affordable refit feel equally urgent.

Known limitations:
- The multi-hop route planner selects the next hop; it does not auto-travel the full route yet.
- Storm Keel temporary current creation is still not implemented.
- Storm Keel Core recovery is marked as future content.
- Faction permits/blockades remain warning/event based rather than full diplomacy.
- Combat remains modal/panel-based rather than tactical 3D.
- Fortress rooms are still list-based, not hex-module placement.
- Audio/music is still hook-only with no external assets bundled.

Recommended next patch:
- Route planner polish and route event expansion, or
- deeper faction gate diplomacy/permits/blockades, or
- Storm Keel Core/research progression, or
- fortress hex module builder foundation.
