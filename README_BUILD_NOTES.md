# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.19.2223

Focused gameplay-video QA and first roadmap implementation pass.

## Patch Intent

- Fix clear issues observed in the 61-second new-campaign gameplay recording.
- Improve early onboarding clarity without redesigning the game.
- Start the safest roadmap/bible item: post-tutorial Open Command directives after Captain's Orders.
- Preserve gate-locked Current Gate / Jet Stream travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, singleton music behavior, and current combat balance.

## Video Findings Addressed

- Bottom-left music debug text clipped in the command panel.
- Right upgrade panel could feel stuck deep in the list after upgrades.
- Multi-hop route plotting worked, but could read as though the Navigator was sending the player backward because the next hop replaced the selected final target.
- Travel-in-progress state was functional but too subtle.
- Disabled Launch Skiffs button did not explain that a Hangar room is required.
- Post-tutorial Open Command existed but needed clearer campaign directives.

## Fixes Made

- Hid the debug music line by default so audio status no longer clips the command panel.
- Added a reliable right-panel scroll reset after content rerenders.
- Reworded Clockwork Navigator route cards and toasts to separate Final Destination from Current Jump / Next Hop.
- Added an in-panel travel status cue while Brasswake is riding a Current.
- Added a disabled combat reason for Launch Skiffs.
- Reworked Next Campaign Goals into roadmap-aligned Open Command Directives: Chart, Secure, Prepare, and Investigate.

## Roadmap/Bible Alignment

- Implements the safest slice of the Post-Tutorial Campaign Goal Pass.
- Keeps Open Command as guidance rather than a new mechanic, avoiding risk to balance, routes, saves, or combat.
- Reinforces the bible direction that Captain's Orders should lead into broader strategic command goals.

## Systems Intentionally Preserved

- No early freeform direct travel was restored.
- Gate-locked Current Gate / Jet Stream travel remains the primary travel method.
- Clockwork Navigator / Celestial Navigation Automaton remains installed at campaign start.
- Plot Capacity remains 1 Jump.
- Combat balance was not changed.
- Music remains singleton-managed: one active loop and one optional fading loop; stingers remain non-looping.
- MP3 files remain external under `assets/audio/music/`.
- The build remains a single-file HTML game using the Three.js CDN.

## Validation Performed

- Extracted JavaScript from `index.html` and ran `node --check`.
- Checked inline `onclick` handlers for missing global function references.
- Checked duplicate function declarations.
- Checked version strings for `v0.26.06.19.2223`.
- Confirmed Three.js CDN reference remains.
- Confirmed music paths remain relative under `assets/audio/music/`.
- Confirmed no audio base64 embedding.
- Created ZIP package with `index.html`, external assets, manifest, README, and build notes.

## Deferred

- Storm Keel, Saint Elmo Core, Astrolabe Engine, Plot Capacity 2+, faction permit systems, full fortress module visuals, and combat presentation expansion remain future roadmap work.
