IRON KINGDOMS: SKY FORTRESS COMMAND
Version: v0.26.06.20.1139

Focused Navigator audio stabilization and first-session polish patch.

PATCH INTENT
- Address the player-reported double-music issue in the Captain's Orders route-to-Danger-1 flow.
- Keep the Clockwork Navigator / Celestial Navigation Automaton clear without restoring early freeform travel.
- Improve post-tutorial Open Command readability in the lower-right HUD.
- Preserve combat balance, gate-locked travel, external music assets, and the single-file HTML build.

ISSUES ADDRESSED
- Two music tracks could be heard after using Captain's Orders to plot/navigate toward a Danger 1 enemy with the Clockwork Navigator.
- Route-lock stingers could feel like a second music bed if they lasted too long over a newly selected Navigator loop.
- Combat-result music restore used a delayed callback that could become stale after later UI or music-state changes.
- Old direct-engine travel helper text remained a regression hazard.
- Open Command post-tutorial copy was too dense for the lower-right HUD.
- The Command box occupied lower-left space that the Selected Location panel needed.
- Captain's Orders was too small when tucked into the bottom corner.
- Old patch-era comments still mentioned a prior build label.

FIXES MADE
- Clockwork Navigator route plotting now hard-settles the prior loop before playing Navigator music.
- Route-lock stingers now use a shorter, quieter playback cap and self-clean even if the audio file is long.
- Stinger cleanup now keeps the main loop ducked only while active stingers remain.
- Combat-result music restore now checks a token and the current loop state before restoring context.
- Direct-engine travel confirmation is hard-disabled and routes back to the No Charted Current / Clockwork Navigator flow.
- Compact Open Command now uses a short directive summary: Chart, Secure, Prepare, Investigate.
- Command controls now live behind a compact Command Menu button.
- Captain's Orders now mirrors Fortress Status as a left-side panel.
- Selected Location now extends farther down the left HUD for better readability.
- Removed stale prior-build wording from CSS comments.
- Removed the unused result-modal callback parameter.

ROADMAP/BIBLE ALIGNMENT
- First-session golden path: select nearby site, ride a charted Current, resolve event, upgrade or repair, plot one Current jump toward a Danger 1 fleet, win or survive combat, then transition to Open Command.
- Official system name: Celestial Navigation Automaton.
- Public nickname: Clockwork Navigator.
- Starting Plot Capacity: 1 Current Gate jump.
- Open Command remains the post-Captain's Orders campaign planner.

RECOMMENDED NEXT 3-5 PATCHES
- Add a small manual audio QA checklist or unobtrusive debug reveal for current loop, fading loop, and stinger state.
- Expand route progression with Navigator upgrades, route memory, faction toll previews, and gate-permit clarity.
- Improve Brasswake management readability by tying rooms/upgrades to stronger fortress status cues.
- Add early combat readability polish without changing current balance.
- Expand faction gate policy and route-event bible notes into playable tutorial hints.

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
- Duplicate function declarations checked.
- Version strings checked for v0.26.06.20.1139.
- Three.js CDN reference checked.
- Relative external music paths checked.
- Referenced music files checked.
- No embedded audio data URLs found.
- No embedded playable preview created.

DEFERRED
- Storm Keel, Saint Elmo Core, Astrolabe Engine, Plot Capacity 2+, faction permit systems, full fortress module visuals, and combat presentation expansion.
- Live browser/audio repro should still be done on the Captain's Orders -> Plot Route to Danger 1 Fleet -> Ride Locked Jump -> Combat path.
