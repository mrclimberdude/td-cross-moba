# Source Folder

This folder is the starting point for the gameplay code for the TD/MOBA prototype.

## Intended layout

- Public/
  - gameplay-facing declarations and interfaces
  - data structures and API surfaces used by gameplay systems
- Private/
  - implementations and gameplay logic
  - class definitions and system behavior

## Initial intent

The codebase is intentionally kept small and modular so the prototype can validate:
- TD placement and route shaping
- MOBA combat and movement
- minion behavior and wave logic
- resource collection and economy flow
- objective and win-state logic

Keep gameplay responsibilities separated by role and system so the project stays readable while the prototype is being developed.
