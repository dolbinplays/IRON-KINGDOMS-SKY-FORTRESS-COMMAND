# IRON KINGDOMS: SKY FORTRESS COMMAND - v0.26.06.20.1139

Focused Navigator audio stabilization and first-session polish patch.

## Patch Intent

- Address the player-reported double-music issue in the Captain's Orders route-to-Danger-1 flow.
- Keep the Clockwork Navigator / Celestial Navigation Automaton clear without restoring early freeform travel.
- Improve post-tutorial Open Command readability in the lower-right HUD.
- Preserve combat balance, gate-locked travel, external music assets, and the single-file HTML build.

## Issues Addressed

- Two music tracks could be heard after using Captain's Orders to plot/navigate toward a Danger 1 enemy with the Clockwork Navigator.
- Route-lock stingers could feel like a second music bed if they lasted too long over a newly selected Navigator loop.
- Combat-result music restore used a delayed callback that could become stale after later UI or music-state changes.
- Old direct-engine travel helper text still existed in source as a regression hazard even though the live flow used gate-locked Current travel.
- Open Command post-tutorial copy was too dense for the lower-right HUD.
- The Command box occupied lower-left space that the Selected Location panel needed.
- Captain's Orders was too small when tucked into the bottom corner.
- Old patch-era comments still mentioned a prior build label.

## Fixes Made

- Clockwork Navigator route plotting now hard-settles the prior loop before playing Navigator music.
- Route-lock stingers now use a shorter, quieter playback cap and self-clean even if the audio file is long.
- Stinger cleanup now keeps the main loop ducked only while active stingers remain.
- Combat-result music restore now checks a token and the current loop state before restoring context.
- Direct-engine travel confirmation is hard-disabled and routes back to the No Charted Current / Clockwork Navigator flow.
- Compact Open Command now uses a short directive summary: Chart, Secure, Prepare, and Investigate.
- Command controls now live behind a compact Command Menu button.
- Captain's Orders now mirrors Fortress Status as a left-side panel.
- Selected Location now extends farther down the left HUD for better readability.
- Removed stale prior-build wording from CSS comments.
- Removed the unused result-modal callback parameter.

## Roadmap/Bible Alignment

- First-session golden path remains: select a nearby site, ride a charted Current, resolve the event, upgrade or repair, plot one Current jump toward a Danger 1 fleet, win or survive combat, then transition to Open Command.
- The official system name remains Celestial Navigation Automaton; Clockwork Navigator is the public nickname.
- Starting Plot Capacity remains 1 Current Gate jump.
- Open Command remains the post-Captain's Orders campaign planner rather than a balance-changing mechanic.

## Recommended Next 3-5 Patches

- Add a small manual audio QA checklist or unobtrusive debug reveal for current loop, fading loop, and stinger state.
- Expand route progression with Navigator upgrades, route memory, faction toll previews, and gate-permit clarity while keeping Plot Capacity 1 at campaign start.
- Improve Brasswake management readability by tying rooms/upgrades to stronger fortress status cues.
- Add early combat readability polish without changing the current balance.
- Expand faction gate policy and route-event bible notes into playable tutorial hints.

## Systems Intentionally Preserved

- No early freeform direct travel was restored.
- Gate-locked Current Gate / Jet Stream travel remains the primary travel method.
- Clockwork Navigator / Celestial Navigation Automaton remains installed at campaign start.
- Plot Capacity remains 1 Jump.
- Captain's Orders and Open Command are preserved.
- Combat balance was not changed.
- Music remains singleton-managed: one active loop plus one optional fading loop during crossfade; stingers remain non-looping.
- MP3 files remain external under `assets/audio/music/`.
- The build remains a single-file HTML game using the Three.js CDN.

## Validation Performed

- Extracted JavaScript from `index.html` and ran syntax validation.
- Checked inline `onclick` handlers for missing global function references.
- Checked duplicate function declarations.
- Checked version strings for `v0.26.06.20.1139`.
- Confirmed Three.js CDN reference remains.
- Confirmed music paths remain relative under `assets/audio/music/`.
- Confirmed referenced music files exist.
- Confirmed no embedded audio data URLs.
- No embedded playable preview was created.

## Deferred

- Storm Keel, Saint Elmo Core, Astrolabe Engine, Plot Capacity 2+, faction permit systems, full fortress module visuals, and combat presentation expansion remain future roadmap work.
- A live browser/audio repro pass should still be done by playing the exact Captain's Orders -> Plot Route to Danger 1 Fleet -> Ride Locked Jump -> Combat path in a browser.
