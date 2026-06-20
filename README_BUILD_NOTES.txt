IRON KINGDOMS: SKY FORTRESS COMMAND
Music Integration Patch
Version: v0.26.06.19.music

Build contents:
- index.html
- assets/audio/music/loops/
- assets/audio/music/stingers/

Patch summary:
- Updated visible title, version label, VERSION constant, SAVE_KEY, package folder, and build notes to v0.26.06.19.music.
- Added a browser-safe JavaScript music manager with track registry, state-based loop playback, stingers, crossfading, user-interaction audio unlock, mute toggle, volume slider, localStorage music settings, and missing-file fail-safes.
- Copied and renamed generated MP3s into web-safe lowercase snake_case filenames under assets/audio/music/.
- Registered primary and alternate music variants for map, Brasswake management, Navigator, route types, locations, combat types, factions, late-game, Storm Keel, and credits.
- Wired high-confidence existing game states: title, new campaign/tutorial, map/arrival contexts, right-panel tabs, Navigator plotting, Current travel by route type, location events, pre-combat/combat, victory, defeat, retreat, Saint Elmo boost, and Storm Keel unlock.
- Preserved gate-locked Current Gate travel, route/event logic, combat balance, and the existing single-file HTML code approach.

Browser note:
Most browsers block autoplay. Music begins only after the first player click/tap/key press.

Validation performed:
- JavaScript extracted from index.html and checked with node --check.
- Version strings checked for consistency.
- Music files copied/renamed from the uploaded ZIP.

Missing source files while packaging:
- None
