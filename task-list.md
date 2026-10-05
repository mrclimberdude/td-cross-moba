# TD/MOBA Prototype Task List

## Overall Goal
Build a small, testable prototype that proves the core asymmetric loop:
- TD player shapes the battlefield through towers, barriers, and spawners
- MOBA player fights, gathers resources, and pushes the objective
- The team wins by coordinating both roles toward base destruction

## Prototype Scope Lock
- [ ] 1 TD player
- [ ] 1 MOBA player
- [ ] 1 broad-plane map
- [ ] 1 minion spawner
- [ ] 1 resource node
- [ ] 1 enemy base objective
- [ ] Simplified resource loop: MOBA gathers resources to fund TD build budget
- [ ] Local prototype first (no advanced networking or lobby features yet)

## Week 1: Project Setup and Core Prototype Definition
- [ ] Create Unreal project structure and basic gameplay framework
- [ ] Set up a test map with one broad plane, base, resource node, and spawner
- [ ] Define TD role and MOBA role gameplay split
- [ ] Create basic debug UI for:
  - [ ] player role
  - [ ] resources
  - [ ] selected structure
  - [ ] active objective
- [ ] Decide and implement the first-pass economy rule
- [ ] Lock the first playable prototype target
- [ ] Ensure a basic loop exists: spawn minion -> route path -> MOBA fights -> objective can be destroyed
- [ ] Verify the prototype runs in a test level

## Week 2: TD Build and Route Manipulation
- [ ] Build the TD top-down camera and interaction system
- [ ] Implement tower placement
- [ ] Implement barrier placement
- [ ] Implement spawner placement or upgrade
- [ ] Add placement validation rules
- [ ] Implement minion pathing based on placed obstacles and towers
- [ ] Add route preview before placement
- [ ] Implement basic minion AI movement and targeting
- [ ] Add simple tower damage behavior
- [ ] Make building and route changes readable in the map
- [ ] Verify a TD placement changes the minion route in a clear, understandable way

## Week 3: MOBA Combat and Resource Loop
- [ ] Create a simple first-person or close-quarters combat controller
- [ ] Add movement, aiming, and attack or shooting behavior
- [ ] Implement enemy minion AI
- [ ] Add resource collection interaction at the resource node
- [ ] Transfer collected resources into the TD build economy
- [ ] Add destructible enemy towers and barriers
- [ ] Add basic enemy aggression and engagement behavior
- [ ] Add a base objective with health and destruction state
- [ ] Verify the MOBA player can fight minions and damage structures
- [ ] Verify the collection loop affects TD build capability

## Week 4: Full Loop Polish and Playtest
- [ ] Connect the full end-to-end loop:
  - [ ] MOBA collects resources
  - [ ] TD spends resources to build and place structures
  - [ ] Minions spawn and follow route
  - [ ] MOBA fights through minions and defenses
  - [ ] Team pushes the base objective
- [ ] Add basic UI for:
  - [ ] TD build budget
  - [ ] MOBA resource count
  - [ ] base health
  - [ ] minion wave status
- [ ] Add basic sound and visual feedback for placement, combat, and objective damage
- [ ] Run internal playtest sessions
- [ ] Record observations on readability, role split, and fun factor
- [ ] Determine whether the loop feels like a convincing prototype
- [ ] Identify next improvement priorities based on playtest feedback

## Explicit Scope Exclusions for Month 1
- [ ] Full matchmaking / lobby systems
- [ ] Advanced fog-of-war
- [ ] Multiple lanes or large map variants
- [ ] More than one resource node
- [ ] Long-term progression systems
- [ ] Advanced hero ability kits
- [ ] Large-scale AI behavior
- [ ] Full economy balancing
- [ ] High-end visual polish

## Open Questions to Resolve Early
- [ ] How exactly TD resources are generated over time
- [ ] Whether spawn resources and build resources should be separate currencies
- [ ] Whether the prototype should stay at 1 TD + 1 MOBA or expand to more MOBA players
- [ ] Whether to keep the map as a single broad plane for now

## Success Criteria for the Prototype
- [ ] A tester can understand the roles without a long explanation
- [ ] The TD player can meaningfully shape combat with placement decisions
- [ ] The MOBA player can fight through minions and contest space
- [ ] The resource loop creates pressure and consequence
- [ ] The team can coordinate a push to the enemy base
- [ ] The core fantasy feels clear and playable

## Notes
This task list is intentionally minimal and focused. Month 1 is about proving the core loop, not building a full production game.
