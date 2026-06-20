IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.19.2223

Focused gameplay-video QA and first roadmap implementation pass.

PATCH INTENT
- Fix clear issues observed in the new-campaign gameplay recording.
- Improve early onboarding clarity without redesigning the game.
- Start the safest roadmap/bible item: post-tutorial Open Command directives.
- Preserve gate-locked travel, Clockwork Navigator, Plot Capacity: 1 Jump, Captain's Orders, singleton music, and combat balance.

VIDEO FINDINGS ADDRESSED
- Music debug text clipped in the command panel.
- Right upgrade panel could feel stuck deep in the list after upgrades.
- Multi-hop route plotting needed clearer Final Destination vs Current Jump wording.
- Travel-in-progress state was too subtle.
- Disabled Launch Skiffs button needed a reason.
- Open Command needed clearer post-tutorial campaign directives.

FIXES MADE
- Hid the debug music line by default.
- Added right-panel scroll reset after rerenders.
- Clarified Clockwork Navigator route cards and toasts.
- Added an in-panel travel status cue while riding a Current.
- Added Launch Skiffs disabled reason: requires Hangar.
- Reworked Next Campaign Goals into Open Command Directives: Chart, Secure, Prepare, Investigate.

ROADMAP/BIBLE ALIGNMENT
- Implements the safest slice of the Post-Tutorial Campaign Goal Pass.
- Keeps Open Command as guidance, not a new balance-affecting mechanic.
- Reinforces the transition from Captain's Orders to broader strategic command.

PRESERVED
- No early freeform direct travel.
- Gate-locked Current Gate / Jet Stream travel.
- Clockwork Navigator / Celestial Navigation Automaton.
- Plot Capacity: 1 Jump.
- Current combat balance.
- Singleton music behavior.
- External MP3 assets under assets/audio/music/.
- Single-file HTML game using Three.js CDN.

VALIDATION
- JavaScript extracted from index.html and checked with node --check.
- Inline onclick handlers checked for missing global functions.
- Duplicate function declarations checked.
- Version strings checked for v0.26.06.19.2223.
- Three.js CDN reference checked.
- Relative external music paths checked.
- No audio base64 embedding found.

DEFERRED
- Storm Keel, Saint Elmo Core, Astrolabe Engine, Plot Capacity 2+, faction permit systems, full fortress module visuals, and combat presentation expansion.
