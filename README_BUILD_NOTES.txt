IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.20.1245

Focused directional fortress travel patch.

PATCH INTENT
- Make Brasswake visually face the direction of each Current Gate / Jet Stream jump.
- Treat the left-pointing segment of the current procedural fortress model as the bow/front.
- Preserve gate-locked travel, Clockwork Navigator rules, Plot Capacity: 1 Jump, Captain's Orders, singleton music, combat balance, and the single-file HTML build.

ISSUES ADDRESSED
- Brasswake could slide from one hex to another without first facing the destination.
- The render loop applied a decorative yaw sway every frame, which would prevent persistent travel heading.
- Older saves had no stored fortress-facing field.

FIXES MADE
- Added persistent game.fortressFacing state with a safe default for new and loaded campaigns.
- Added angle normalization and shortest-turn helpers for stable Three.js Y rotation.
- Added destination-facing math that treats the model's local/world -X direction as the bow.
- Updated travel animation to rotate in place first, then move along the current jump.
- Updated map rebuild/position refresh to restore the saved fortress facing.
- Removed the old idle yaw override so Brasswake remains pointed in its last travel direction after arrival.

PRESERVED
- No early freeform direct travel.
- Gate-locked Current Gate / Jet Stream travel.
- Clockwork Navigator / Celestial Navigation Automaton.
- Plot Capacity: 1 Jump.
- Captain's Orders and Open Command.
- Current combat balance.
- Singleton music behavior.
- External MP3 assets under assets/audio/music/.
- Single-file HTML game using Three.js CDN.

VALIDATION
- JavaScript extracted from index.html and syntax checked.
- Inline onclick handlers checked for missing global functions.
- Version strings checked for v0.26.06.20.1245.
- Three.js CDN reference checked.
- Relative external music paths checked.
- Referenced music files checked.
- No embedded audio data URLs found.
- No embedded playable preview created.

DEFERRED
- No route-rule changes, combat balance changes, music-system changes, or fortress model redesigns were attempted.
- Live browser/game-feel verification should still be done by riding a one-hop Current and then a continued plotted route.
