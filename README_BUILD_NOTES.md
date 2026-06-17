# IRON KINGDOMS: SKY FORTRESS COMMAND — v0.26.06.17.0300

## Package Contents

- `index.html` — standalone single-file browser build.

## Version Consistency

- Displayed version label: v0.26.06.17.0300
- VERSION constant: v0.26.06.17.0300
- Save key: IK_SKY_FORTRESS_COMMAND_v0_26_06_17_0300
- Package/folder name: IRON_KINGDOMS_SKY_FORTRESS_COMMAND_v0.26.06.17.0300

## Summary of Changes

- Fixed selected-location panel scroll retention when selecting a new map node.
- Depleted enemy fleets no longer show active Combat Readiness; cleared enemy sites now show a resolved/secured state.
- Captain’s Orders now uses “Next Order” language so out-of-order progress feels intentional rather than broken.
- Free ruin/research upgrades now count as fortress improvement for the tutorial objective.
- Added stronger one-time first-upgrade guidance and preferred early upgrade ordering for Engines, Armor, and Weapons.
- Made Current Gates matter more by expanding the route web, making current travel cheaper, and making direct engine travel more expensive.
- Added low-risk direct-travel hull strain for longer uncharted direct routes.
- Added simple Jet Stream route events for tolls, turbulence, patrol/salvage-style outcomes, and smooth-current travel logs.
- Improved Current Gate visuals with vertical vane-rings, brass pylons, and route-type glow so gates no longer read like selection rings.
- Improved route hierarchy: brighter Current routes, dim dashed direct fallback lines, and a route legend in Help/Build Notes.
- Added dynamic fantasy-steampunk current-travel text based on route type, departure, destination, and owner.
- Updated the hex board to use true touching hex tile geometry with subtle grooves instead of visible open gaps.

## Known Limitations

- Current Gates are still a foundation system; full faction toll/blockade/permit logic is not complete.
- Direct travel still exists as a safety fallback, though it is now less efficient and can lightly strain the hull.
- Route events are lightweight log/toast outcomes, not full encounters.
- Storm Keel temporary-current engine is not implemented yet.
- Fortress hex module construction is not implemented yet.
- Tactical 3rd-person fortress flight is not implemented yet.
- Combat remains panel-based.
- Saves from earlier versions use different save keys and will not auto-load in this build.

## Recommended Next Patch

Recommended next patch: expand the Current Gate system with faction-controlled tolls, blockades, permits, and route event variety, or begin the Storm Keel / temporary current unlock foundation once route logic feels stable.
