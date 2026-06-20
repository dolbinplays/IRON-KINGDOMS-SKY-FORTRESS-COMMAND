IRON KINGDOMS: SKY FORTRESS COMMAND
Emergency Steel Recovery / Economy Safety Patch
Version: v0.26.06.20.1322

SOURCE OF TRUTH CHECK
- Uploaded source title version: v0.26.06.18.1400
- Uploaded source visible versionLabel: v0.26.06.18.1400
- Uploaded source VERSION constant: v0.26.06.18.1400
- Uploaded source SAVE_KEY: IK_SKY_FORTRESS_COMMAND_v0_26_06_18_1400
- Target patch version used: v0.26.06.20.1322
- Note: the uploaded file mounted for this patch did not contain the newer external MP3 music manager/audio integration. No audio assets were embedded or modified.

PATCH SUMMARY
Added a limited, reliable emergency steel recovery option at skyports and settlements:
- Dockyard Scrap Purchase: 20 Gold -> 10 Steel
- Available only while Brasswake is at a skyport or settlement
- Limited to once per campaign day through game.flags.lastScrapPurchaseDay
- Does not advance day
- Does not damage hull
- Sets returnedForService
- Adds a log entry
- Shows clear toast feedback
- Autosaves and re-renders the UI

STEEL ECONOMY PRESERVED
The patch did not broadly rebalance existing steel sources or costs. Existing steel sources remain primary:
- Salvage wreck fields
- Steel resource nodes
- Ruins
- Combat victory
- Emergency Drift/Scavenge chance
- Foundry steel bonuses

Existing steel spending remains intact:
- Port repairs
- Room construction
- Upgrade purchases
- Combat emergency repairs
- Storm Keel research costs

ROADMAP / BIBLE UPDATE
The in-game Help, Build Notes, Navigation Doctrine, Next Campaign Goals, and Future Balance Review now document the Emergency Steel Recovery Valve. Future tuning hooks are noted for faction pricing, stock limits, Foundry conversion bonuses, industrial skyport discounts, hostile blockade markups, and black-market bulk scrap.

PRESERVED
- Single-file HTML structure
- Existing Three.js CDN approach
- Gate-locked Current Gate / Jet Stream travel
- No early freeform direct travel
- Clockwork Navigator / Celestial Navigation Automaton
- Plot Capacity: 1 Jump
- Captain's Orders onboarding
- Modular Brasswake rooms/upgrades/status
- Route plotting and route events
- Existing combat balance
- Save/load/autosave behavior, with older-save-safe flag defaults

VALIDATION PERFORMED
- Extracted JavaScript and ran node --check successfully
- Checked inline onclick handlers; no missing function references found
- Confirmed all version strings use v0.26.06.20.1322
- Confirmed SAVE_KEY uses IK_SKY_FORTRESS_COMMAND_v0_26_06_20_1322
- Confirmed Dockyard Scrap Purchase is rendered only inside the skyport/settlement service block
- Confirmed the purchase function validates location, daily limit, steel cap, and gold cost
- Confirmed repair, fuel purchase, and settlement contract functions were preserved
- Confirmed no route/travel/combat systems were rewritten
- No embedded playable preview was created

IMPORTANT SOURCE NOTE
The uploaded source file for this patch reported v0.26.06.18.1400. If you intended to patch a newer local build such as v0.26.06.20.1245 with music integration and directional travel, do not overwrite that newer build with this package. Upload that newer index.html and this same patch can be applied there.
