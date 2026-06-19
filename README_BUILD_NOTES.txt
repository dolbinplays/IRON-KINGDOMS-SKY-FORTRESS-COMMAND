IRON KINGDOMS: SKY FORTRESS COMMAND — v0.26.06.18.1400

Patch: First Session Flow + Roadmap Foundation

Primary goals completed:
- First Session Flow polish.
- Selected Location scroll/top-context fix.
- Current-location action ordering improvements.
- Captain's Wings clipping fix by hiding the compact decorative wing badge in bottom-right Open Command mode.
- State-aware Captain's Orders route nudges.
- Route-event wording polish with route-type-aware clean-passage labels.
- Clockwork Navigator / Plot Capacity rules preserved.
- Storm Keel remains locked; no temporary current creation was added.
- Saint Elmo Core and Astrolabe Engine remain future hooks.
- Roadmap/bible foundation expanded in Help, Tech, Build Notes, and Open Command next-goal guidance.

Preserved systems:
- Three.js overworld.
- Procedural edge-to-edge hex-board layout.
- Current Gate / Jet Stream route network.
- Gate-locked early strategic travel.
- No early freeform direct overworld bypass travel.
- Multi-hop Current Gate route planner.
- Persistent plotted-route context.
- Eventful Current travel overlay.
- Faction route events, tolls, permit/inspection/blockade warnings.
- Clockwork Navigator / Celestial Navigation Automaton UI.
- Plot Capacity: 1 jump.
- Captain's Orders tutorial flow.
- Captain's Wings / Open Command post-tutorial behavior.
- Modular Brasswake marker.
- Salvage, harvest, trade, repair, contracts, storms, ruins, combat.
- Upgrades / rooms / factions / tech tabs.
- Autosave/manual save/load/reset.

Roadmap/bible notes added:
- Celestial Navigation Automaton is the official navigation-system name.
- Clockwork Navigator is the common/public nickname.
- Starting Plot Capacity is 1 Current Gate jump.
- Plot Capacity 1 means the automaton locks only the next Current Gate jump while the captain keeps final-destination context.
- Future upgrades can increase plot capacity.
- Saint Elmo Navigation Core is a future advanced navigation component/upgrade.
- Astrolabe Engine is a future alternate built-in navigation system for craft that do not use an onboard automaton.
- Storm Keel Engine remains locked mid/late-game technology for temporary current/conduit creation.
- Brasswake should continue evolving toward a modular flying fortress/city, not just a ship token.
- Future roadmap includes faction gate diplomacy, route permits, inspections, blockades, and room/module visual links.

Future balance review notes:
- Starting resource generosity.
- Early upgrade pacing.
- Danger 1 combat difficulty after multiple early upgrades.
- Repair pressure.
- Fuel pressure over longer routes.

Validation performed:
- Uploaded source inspected before patching and confirmed as v0.26.06.18.1300.
- Patched title, visible versionLabel, VERSION constant, SAVE_KEY, and title-screen build note to v0.26.06.18.1400.
- Confirmed no old v0.26.06.18.1300 or v0.26.06.18.1200 text remains in the patched HTML.
- Extracted JavaScript from index.html and ran node --check successfully.
- Confirmed direct fallback route drawing remains disabled.
- Confirmed Storm Keel remains locked/future and no temporary current creation was implemented.
- No embedded playable preview was created.

Suggested next steps:
1. Run a fresh new-game recording and verify the Selected Location panel starts at the top after selection, plotting, arrival, event completion, combat completion, and harvest completion.
2. Start a second pass on Clockwork Navigator upgrade tiers: Plot Capacity 1 -> 2 -> 3.
3. Expand faction gate diplomacy with permits, inspections, favored routes, and blockade states.
4. Add visible Brasswake module links to rooms/upgrades.
5. Begin Saint Elmo Navigation Core recovery/install content after the route UX is stable.
