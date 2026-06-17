IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.17.0001

Package contents:
- index.html
- README_BUILD_NOTES.txt

How to run:
Open index.html in a modern browser with an internet connection. This prototype loads Three.js from the jsDelivr CDN.

Implemented systems:
- Single-file HTML/CSS/JavaScript browser build
- Three.js stylized 3D strategic map
- Procedural world with skyports, settlements, salvage fields, resources, storms, ruins, contracts, and enemy fleets
- Iron Kingdoms faction integration and standing bands
- Click-to-select world nodes and fuel-consuming travel
- Fortress stats, resources, rooms, and upgrades
- Resource loop: salvage, harvest, trade, repair, contracts, ruins, storm rewards, emergency drift
- Turn-based fortress combat with main guns, skiffs, bracing, emergency repairs, retreat, victory rewards, and defeat consequences
- AI/world simulation events and simple faction fleet movement
- LocalStorage save/load/reset with version metadata
- Title screen, event log, command panels, build notes, help modal, and polished Iron Kingdoms UI styling

Known limitations:
- Room placement is simplified to build slots, not a spatial interior grid yet
- Combat is a tactical panel with 3D context rather than a full spatial Stratosphere-style battlefield
- Diplomacy is intentionally simple for Phase 1
- AI faction behavior is lightweight and event-driven
- Audio is hook-only/no external assets
- Three.js requires internet access for the CDN in this version

Suggested Phase 2:
- Add internal fortress grid placement and room adjacency bonuses
- Add officer/crew portraits and crew personality events
- Add boarding missions and wreck interiors
- Add faction-specific fortress skins and campaign starts
- Expand diplomacy, treaty, raid, and reputation systems
- Add deeper research tree and unique tech unlocks
- Add escort/custom fleet craft
- Add music and SFX asset integration
- Add optional cloud save or asynchronous multiplayer sharing
