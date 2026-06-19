IRON KINGDOMS: SKY FORTRESS COMMAND v0.26.06.18.1200

Source verification:
- Patched from verified source: /mnt/data/IRON_KINGDOMS_SKY_FORTRESS_COMMAND_v0.26.06.18.1000/index.html
- Source version before patch: v0.26.06.18.1000
- Captain's Wings / Open Command behavior present: yes
- Modular Brasswake marker present in source before patch: no — restored from the v0800 procedural marker line

Patch summary:
- Updated all visible/build/save/package version references to v0.26.06.18.1200.
- Rebuilt Selected Location and right-side panels as flex-column shells with header/tabs outside scroll bodies.
- Added scrollContent bottom gutters so long panel content can scroll to the true bottom.
- Cleaned Captain's Wings / Open Command completed-state layout so text, alert, and badge do not overlap.
- Restored the lightweight procedural modular Brasswake hex-fortress marker using built-in Three.js geometry only.
- Added subtle arc-lift ring animation/glow support for the restored Brasswake marker.
- Added clearer Danger 1 guidance when Captain's Orders still needs low-danger combat and the selected enemy is Danger 2+.
- Updated in-game build notes with v1200 source-consolidation and roadmap notes.

Known limitations:
- Multi-hop route plotting still selects the next hop rather than auto-traveling the full route.
- Storm Keel temporary current creation remains locked for a future patch.
- Visible Brasswake modules are not yet tied to actual rooms/upgrades/damage states.
- Combat remains panel-based rather than tactical 3D.
- Faction permits/blockades remain lightweight event/warning systems.

Validation performed:
- JavaScript syntax extracted and checked with node --check.
- Version string consistency checked.
- Package/ZIP integrity checked.
- Static source checks confirmed panel shell classes, Captain's Wings cleanup, restored modular marker, and Danger 1 guidance are present.
