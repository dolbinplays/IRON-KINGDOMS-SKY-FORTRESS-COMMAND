IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.19.2148

Focused QA stabilization pass.

SOURCE OF TRUTH CHECK
- Title before patch used the previous suffixed music build label
- Visible versionLabel before patch used the previous suffixed music build label
- VERSION before patch used the previous suffixed music build label
- SAVE_KEY before patch used the previous suffixed music build label
- Build notes before patch mixed older HUD-polish and music-integration labels
- External music paths are referenced under assets/audio/music/
- Build appears to be the music singleton / double-play prevention build

FINDINGS
Critical: no syntax crash found.
High: stale version/build-note strings; failed next-loop crossfade could lose the intended active loop.
Medium: save/load/reset and save-status paths needed storage/DOM guards; stinger play-block warnings could repeat.
Low: README/package notes were stale.

FIXES MADE
- Aligned title, visible label, VERSION, SAVE_KEY, manifest, README files, and in-game notes to v0.26.06.19.2148.
- Hardened save/load/reset and save-status UI flows.
- Restored the previous fading loop as active if a new music loop fails during crossfade.
- De-duplicated stinger play-block warnings.
- Added small null guards for toast, modal, log, version-label, and title load-button updates.

PRESERVED
- Gate-locked Current Gate / Jet Stream travel.
- No early freeform direct travel.
- Clockwork Navigator / Celestial Navigation Automaton.
- Plot Capacity: 1 Jump.
- Captain's Orders onboarding.
- Brasswake status, rooms, upgrades, factions, tech, route, travel, and combat systems.
- Existing combat balance.
- External MP3 assets under assets/audio/music/.
- Singleton music behavior with one active loop and one optional fading loop.
- Non-looping stingers.
- No embedded playable preview.

VALIDATION
- JavaScript extracted from index.html and checked with node --check.
- Inline onclick handlers checked for missing global functions.
- Duplicate function declarations checked.
- Version strings checked for v0.26.06.19.2148.
- Relative external music paths checked.
- Three.js CDN single-file HTML approach preserved.
- MP3 files remain external and are not base64 embedded.

OUT OF SCOPE
- Route balance, combat balance, major UI redesign, and new feature work were intentionally left unchanged.
