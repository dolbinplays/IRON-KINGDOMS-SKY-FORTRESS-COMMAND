# IRON KINGDOMS: SKY FORTRESS COMMAND
## Build v0.26.06.17.0100

Focused stabilization and roadmap-foundation patch.

## Implemented

- Updated visible build/version metadata to v0.26.06.17.0100.
- Added Captain's Orders objective tracker for first-time onboarding.
- Added combat readiness previews and confirmation warnings for dangerous fights.
- Tuned early world generation to guarantee a safer starting cluster.
- Reduced early Danger 1 combat spike and improved risk communication.
- Added repair/critical hull warnings and upgrade-available nudges.
- Replaced confusing save status with clearer active/autosave states.
- Added autosave after travel, event resolution, combat, upgrades, room builds, repair/refuel, and emergency drift.
- Added a visible procedural hex-board foundation under the strategic map.
- Improved map readability with hover tooltips, stronger current/selected markers, dimmed depleted locations, and less route-line clutter.
- Improved combat result summaries with hull loss, population loss, resource changes, standing changes, and recommended next action.
- Preserved the single-file HTML + Three.js CDN architecture.

## Known Limitations

- Hexes are currently a visual/structural overworld foundation, not yet a full route-network with Current Gates / Jet Stream Currents.
- Combat remains panel-based; the full 3rd-person tactical fortress flight mode is deferred.
- Fortress rooms are still list/build-slot based; the full fortress hex module builder is deferred.
- Existing saves from v0.26.06.17.0001 use a different save key and will not auto-load in this build.
- Audio hooks exist only as future architecture; no external music/SFX assets are required.

## Recommended Next Patch

Focus on deeper hex-overworld conversion or begin the fortress hex module builder foundation. The next travel roadmap target should be Current Gates / Jet Stream route planning after the hex-board structure is stable.
