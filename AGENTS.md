# AGENTS.md

## Project
This repository is a prototype for a TD/MOBA hybrid game.

The core design is:
- 1 TD player controls the battlefield from a top-down view
- 1 MOBA player fights from a first-person or close-quarters view
- The TD player places towers, barriers, and spawners to shape the route
- The MOBA player gathers resources and pushes toward the enemy base objective
- The team wins by coordinating both roles to destroy the enemy base

## Prototype Goal
The current goal is to validate the core asymmetric loop before expanding the game.

The first playable prototype should prove:
- TD placement meaningfully changes combat flow
- the MOBA player can fight and gather resources
- the resource loop creates pressure and consequence
- the team can coordinate a push to the base

## In Scope
- 1 TD player
- 1 MOBA player
- 1 broad-plane map
- 1 spawner
- 1 resource node
- 1 base objective
- local prototype only
- minimal UI/debug tools
- simple combat and resource loop

## Out of Scope
Do not add or prioritize these until the prototype is proven:
- multiple lanes or large map complexity
- multiple resource nodes
- advanced fog-of-war
- hero roster expansion
- networking or lobby systems
- long-term progression
- large-scale AI
- heavy visual polish
- full economy balancing

## Project Structure Expectations
Keep the project organized by role and system:
- TD: towers, barriers, spawners, placement, route shaping
- MOBA: player combat, movement, weapons, collection
- Enemies: minions and hostile actors
- Shared: game state, match logic, base objective, economy
- Levels: prototype arena and test maps
- UI: shared HUD, role-specific widgets, debug tools

## Development Rules
- Keep the prototype small and readable
- Prefer simple, testable systems over clever complexity
- Keep TD and MOBA systems separate
- Do not add new systems unless they support the core loop
- If a feature does not help validate the prototype, defer it
- Favor clarity and playtesting over polish

## Quality Bar
A feature is not complete unless it:
- supports the TD/MOBA loop
- is readable in play
- is easy to test
- does not expand scope unnecessarily

## Reference
This project direction is based on the current design notes in project-notes.md and the working task list in task-list.md.
