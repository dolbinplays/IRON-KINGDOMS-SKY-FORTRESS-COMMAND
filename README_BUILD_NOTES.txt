IRON KINGDOMS: SKY FORTRESS COMMAND
Build v0.26.06.18.1300

Patch Scope:
Focused Clockwork Navigator clarity and HUD polish patch for the v0.26.06.18.1200 source line.

Implemented:
- Updated visible title, version label, VERSION constant, SAVE_KEY, build notes, package name, and README to v0.26.06.18.1300.
- Added visible Celestial Navigation Automaton / Clockwork Navigator UI.
- Added Plot Capacity: 1 Jump language and rule explanation.
- Consolidated duplicate multi-hop route buttons into a single primary Clockwork Navigator action.
- Improved plotted-route context with final destination, next hop, remaining hops, total path fuel, tolls, highest risk, and route path text.
- Changed awkward multi-hop fuel wording from "Fuel Cost: X Path" to clearer total path fuel language.
- Polished No Charted Current language and reduced repeated Storm Keel warnings.
- Moved primary travel/route action higher in the Selected Location panel.
- Cleaned Captain's Wings / Open Command layout by suppressing the decorative wing badge when alerts would clip it and shrinking the badge in non-alert states.
- Suppressed stale toast messages when the Jet Stream travel overlay opens and simplified post-travel route event notification behavior.
- Added Tech tab roadmap cards for Saint Elmo Navigation Core and Astrolabe Engine future hooks.

Preserved:
- Single-file HTML build.
- Three.js CDN usage.
- Three.js overworld.
- Procedural edge-to-edge hex-board layout.
- Current Gate / Jet Stream route network.
- Gate-locked early strategic travel.
- No early freeform direct overworld bypass travel.
- Multi-hop Current Gate route planner.
- Persistent plotted-route context.
- Eventful current travel overlay and faction-flavored route events.
- Gate tolls, permits/inspection, blockade risk warnings.
- Captain's Orders tutorial progression.
- Captain's Wings / Open Command post-tutorial behavior.
- Modular Brasswake marker.
- Salvage, harvest, trade, repair, contracts, storms, ruins, combat.
- Upgrades / rooms / factions / tech tabs.
- Autosave/manual save/load/reset.

Roadmap/Bible Notes:
- Celestial Navigation Automaton is now visible as the official installed navigation system.
- Clockwork Navigator is now used as the public/common nickname.
- Plot Capacity: 1 Jump is now presented as intentional gameplay.
- Saint Elmo Navigation Core remains a locked advanced navigation component/future installation path.
- Astrolabe Engine remains a future alternate built-in navigation system.
- Storm Keel remains locked mid-to-late-game technology; temporary current/conduit creation was not implemented in this patch.

Suggested Next Steps:
1. Add Clockwork Navigator upgrade levels and route plot capacity upgrades.
2. Add Saint Elmo Core recovery/installation content.
3. Deepen faction gate diplomacy: permits, inspections, toll discounts, blockades, and route event consequences.
4. Tie visible Brasswake hex modules to rooms/upgrades/damage state.
5. After the strategic navigation layer is clearer, prototype the first local fly-around skyspace hex.

Validation:
- JavaScript syntax check passed via node --check after extracting inline script.
- Version consistency confirmed for v0.26.06.18.1300.
- No embedded playable preview was created.
