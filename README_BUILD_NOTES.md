# IRON KINGDOMS: SKY FORTRESS COMMAND v0.26.06.17.0700

## Patch Summary
- Introduced the Celestial Navigation Automaton as the official route-calculation system, with Clockwork Navigator as its crew/public nickname.
- Added visible 1-jump plot capacity language so one-hop route locking feels intentional instead of a UI limitation.
- Added persistent plotted-route context showing final destination, locked next jump, remaining currents, estimated fuel, tolls, and highest risk.
- Added navigator recalculation messages when Brasswake arrives at a gate/anchor during a plotted route.
- Added locked Saint Elmo Navigation Core and Astrolabe Engine roadmap hooks in the Tech tab.
- Clarified that Clockwork Navigator calculates known routes, Saint Elmo improves calculations later, and Storm Keel physically creates temporary currents in a future mid/late-game phase.
- Hardened selected-location panel scroll reset after selection, plotting, travel, modal close, and event/combat results.
- Made pre-first-travel upgrade presentation quieter while keeping optional upgrades available.
- Hid hostile action buttons on depleted enemy locations and reinforced cleared-state text.
- Improved plotted route visual hierarchy with final destination and locked-jump rings plus brighter current-leg highlighting.

## Known Limitations
- The Clockwork Navigator estimates multi-hop routes but only locks the next jump; it does not auto-travel the full route.
- Saint Elmo Navigation Core and Astrolabe Engine are visible roadmap hooks only, not functional upgrade systems yet.
- Storm Keel remains locked and does not create temporary currents in this build.
- Faction permits/blockades remain warning-and-event based rather than full diplomacy.
- Combat is still panel-based rather than a full spatial battle scene.

## Recommended Next Patch
Continue with Navigation Automaton upgrade levels: add limited upgrades that increase plot capacity, improve toll/risk forecasting, and introduce the first Saint Elmo Core recovery/installation event without unlocking Storm Keel temporary current creation yet.
