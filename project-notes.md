# TD/MOBA Hybrid Game Design Document

## 1. Overview

### 1.1 High-level concept
One player takes the role of the tower defense strategist, playing from a standard top-down view of the map. The other players take the role of the MOBA team, playing in first-person or close-quarters combat view, which limits their information and makes the game feel more immediate and tactical.

The TD player is responsible for shaping the battlefield by placing towers and barriers, controlling the flow of minions, and indirectly spawning waves by building or upgrading minion spawners. The MOBA players are responsible for frontline combat, resource collection, map control, and disrupting the enemy side.

The core tension is that the TD player has strategic control over the battlefield, but only the MOBA players can directly patrol, contest objectives, and secure key areas in real time.

### 1.2 Core fantasy
The player fantasy is to act as both battlefield designer and battlefield commander:
- the TD player shapes the map and the enemy’s route
- the MOBA players fight their way through the board and collect the resources needed to sustain that strategy
- both roles must work together to destroy the enemy base

### 1.3 Design intent
This game should feel like a true asymmetric cooperation loop where:
- the TD player manipulates the battlefield
- the MOBA players execute on it
- each role has real strategic value
- the board state evolves over time as the two roles reinforce and counteract each other

### 1.4 Emotional hook
The intended emotional experience is high-risk, high-reward tactical play. The strongest moments should come when a TD player makes a brilliant pathing decision or a clever barrier placement, and the MOBA players then turn that setup into a devastating coordinated push into the enemy base.

The game should reward careful planning, improvisation, and execution under pressure. The biggest payoff is not just winning a fight, but seeing a map setup that was created in advance become a decisive tactical victory.

## 2. Game Structure

### 2.1 Players
- 1 TD player
- multiple MOBA players

### 2.2 Win condition
The win condition is to destroy the enemy base, like in a MOBA.

### 2.3 Minimum viable match structure
The minimum viable map structure is:
- a single broad plane or lane-like area
- enough open space for path manipulation
- a base objective at the end of the route
- key resource locations on the map

### 2.4 Match format
The intended match format is a competitive asymmetric multiplayer encounter where one player plays the TD role and the rest of the team plays as MOBA combatants. The match should feel like a tactical duel between board control and direct front-line execution.

## 3. Roles

### 3.1 TD player role
The TD player plays from a top-down view and is responsible for:
- placing towers
- placing barriers
- shaping the path of minions
- building or upgrading minion spawners
- indirectly generating minion pressure over time
- choosing where to invest resources and build battlefield control

The TD player is strategic and must rely on the MOBA players to attack and defend key spaces effectively.

### 3.2 MOBA player role
The MOBA players play in first-person or close-quarters combat and are responsible for:
- fighting enemy minions
- fighting enemy MOBA players
- gathering resources from key map locations
- protecting collector units or other strategic assets
- destroying enemy towers and barriers
- contesting space and pushing toward the enemy base

### 3.3 Role balance goal
The game is designed so that neither role is optional. The TD player cannot win by themselves because the MOBA players are the ones who directly attack and hold space. The MOBA players cannot win without the TD player’s map control and minion pressure. The ideal match is one where both roles are constantly affecting each other’s decisions.

## 4. Core Gameplay Loop

1. The TD player builds or upgrades minion spawners.
2. The TD player places towers and barriers to shape the pathing of minions.
3. Minions spawn and move through the map according to the TD player’s battlefield decisions.
4. MOBA players gather resources from key map locations and/or protect collector units.
5. MOBA players engage enemy minions and opposing players.
6. MOBA players destroy enemy towers, barriers, and structures.
7. The team pushes toward the enemy base and wins by destroying it.

This loop creates a rhythm of setup, resource contest, battlefield pressure, and objective push.

## 5. Minion and Pathing System

### 5.1 Minion spawning
Minions are spawned indirectly by the TD player through minion spawners.

### 5.2 Pathing
The TD player shapes the pathing of minions by placing towers and barriers. The minions follow the resulting flow of the battlefield.

### 5.3 Map structure for pathing
The lanes are envisioned as broad planes rather than narrow paths, allowing:
- more interesting path manipulation
- multiple possible routes through the same space
- more distinct spawn positions across the near side of the plane
- greater map diversity and emergent strategy

### 5.4 Strategic goal of pathing
The goal of path manipulation is not just to slow enemies down. It is to create opportunities for the MOBA team: redirecting units into vulnerable positions, funneling enemies into a tower line, or opening a lane that allows a coordinated push.

## 6. Resource Model

### 6.1 Current resource direction
The resource loop currently works like this:
- MOBA players gather resources at key points on the map
- or they protect collector units that gather from those locations
- those resources are used to fund the TD player’s build economy
- MOBA players gain experience from offensive actions

### 6.2 TD resource generation
The exact TD resource generation system is still an open question, but the likely direction is that the TD player gains resources primarily from key map locations being mined or collected from.

### 6.3 Currency question
Whether minion spawning resources and tower/barrier construction resources should be the same currency or separate currencies remains open.

### 6.4 Resource economy design goal
The economy should create tension between direct combat, map control, and battlefield preparation. It should reward the MOBA players for doing map work while still giving the TD player meaningful strategic choices about how to spend the resources they receive.

## 7. Map Design

### 7.1 Minimum map structure
The minimum viable map is a single broad-plane lane-like area that includes:
- open pathing space
- resource nodes or mining areas
- a base objective
- enough room for tower and barrier placement

### 7.2 Map goals
The map should support:
- strategic route creation
- MOBA player pressure routes
- contested resource locations
- clear objective pressure toward the enemy base

### 7.3 Proposed map direction
The broad-plane approach is preferable to narrow lanes because it gives the TD player more flexibility to manipulate the battlefield. It also allows multiple spawn positions along the near side of the plane, increasing the variety of possible minion routes and making the battlefield feel more dynamic.

## 8. Player Information and Visibility

### 8.1 TD player visibility
The TD player should have a full map overview with fog-of-war style limits, allowing them to understand the battlefield state without seeing every local event in perfect detail. This gives the TD player strategic oversight while still preserving the tension of hidden or contested map states.

### 8.2 MOBA player visibility
The MOBA players should have limited local vision, with awareness of nearby threats, resource nodes, and major objective events. Their information should be more immediate and tactical than the TD player’s view, reinforcing the first-person action role.

### 8.3 Visibility goal
This system is meant to create asymmetric information rather than arbitrary confusion. The TD player is the strategist, while the MOBA players are the executors. The information difference should reinforce that split without making either role feel blind or unfair.

## 9. Control Scheme and Player Feel

### 9.1 TD player controls
The TD player should use a freeform placement system with some snap rules. Towers and barriers should be placed in a top-down build workflow, allowing for flexible route design while still keeping construction readable and consistent.

### 9.2 MOBA player controls
The MOBA players should feel like fast first-person shooters with abilities. They should be able to move, aim, fight, engage enemies, control space, and participate in frontline combat while also making tactical choices around resources and pressure.

### 9.3 Resource gathering interaction
The resource loop should support both direct collection and protected collector-unit behavior. This gives players multiple ways to interact with the economy and supports the strategic tension between combat and collection.

## 10. Match Flow and Pacing

### 10.1 Match length target
The target match length should be roughly 10–15 minutes. This creates enough time for map setup, resource pressure, and a decisive late-game push without stretching the game into a slow or repetitive grind.

### 10.2 Expected pacing
The match should progress in three phases:
1. Early game: setup, path planning, limited pressure, initial resource contest
2. Mid game: map control becomes important, cargo and collector defense matters, both roles start to influence the board state
3. Late game: a coordinated push becomes decisive, with the TD player’s route shaping and the MOBA team’s combat execution combining into a final objective assault

### 10.3 Pacing goal
The pacing should reward early planning but also allow late-game comebacks. The most satisfying matches are the ones where a strong TD setup leads to a decisive MOBA execution, but the game should still allow the team to recover from a bad opening if they contest resource or battlefield control effectively.

## 11. Player Fantasy and Emotional Hook

The emotional experience is high-risk, high-reward tactical play. The strongest moments happen when a TD player creates a map setup that looks bad at first but becomes devastating once the MOBA team executes it.

The best play moments should feel like:
- a perfect wall or barrier placement redirects minions into a vulnerable position
- the MOBA players exploit that route to push through a dangerous lane
- the team creates an opening that turns into a successful base assault

This creates a satisfying cycle of setup, pressure, and payoff.

## 12. Example Play Scenarios

### 12.1 Scenario 1: route reversal
The TD player places a wall to redirect a minion path around a side route. The MOBA players notice the changed flow and use that lane break to attack an exposed tower line. The enemy side is forced to respond, and the team uses that moment to win a major resource or territory advantage.

### 12.2 Scenario 2: resource defense
The MOBA team is pushing into a contested resource node. The TD player anticipates the danger and shifts a barrier or tower position to protect the route. The team secures the node, gains economy, and converts that into a more dangerous push toward the base.

### 12.3 Scenario 3: late-game objective push
The TD player has spent resources shaping a final route, setting up a minion line that overlaps the enemy’s strongest defensive positions. The MOBA team uses that opening to push through the lane and finish the match with a coordinated objective assault.

## 13. Failure States and Counterplay

### 13.1 TD failure
A significant mistake for the TD player is a poor barrier placement or bad route decision that accidentally opens a path instead of closing one. This creates a direct, readable failure state that can be punished by the opposing team.

### 13.2 MOBA failure
A poor push or failure to protect a resource node can cost the MOBA team pressure and economy. This creates a meaningful consequence for underperforming in the field.

### 13.3 Counterplay design goal
The game should reward smart adaptation. A failing setup should be punishable, but not permanently unrecoverable. If the TD player makes a mistake, the MOBA players should be able to exploit it. If the MOBA team misses a resource fight, the TD player should still have the ability to recover through future map planning.

## 14. Prototype Goals

### 14.1 Minimum prototype scope
The prototype should be intentionally small and focused. A successful first build should demonstrate:
- one TD player
- one MOBA player
- one broad lane or plane
- one minion spawner
- one resource node
- a simple objective at the end of the path

### 14.2 Prototype success conditions
The prototype is successful if it proves that:
- the TD player can meaningfully shape combat by placing towers and barriers
- minions follow the player-created route in a readable way
- the MOBA player can fight through the minions and contest resources
- the resource loop creates meaningful pressure and consequence
- the team can coordinate a push toward the enemy base

## 15. Inspirations

- Sanctum 2: TD/FPS hybrid with path manipulation
- SMITE: MOBA/TPS pace and role-based combat
- Bloons TD Battles: PvP tower defense structure and pressure-based strategy

## 16. Open Questions

The following are still unresolved and should be treated as active design questions for future iteration:
- How exactly the TD player gains resources over time
- Whether minion spawning and build resources should be separate currencies
- How many MOBA players should be included in a match
- How many distinct playable plane or lane structures are needed for the final game
- How broad the overall map should be before the game becomes too complex
- How much information each role should be allowed to see in the final product
- How exactly the TD player and MOBA players coordinate during a match in practice

## 17. Current Working Interpretation

The current working interpretation is:
- 1 TD player with top-down tactical control
- multiple MOBA players with first-person engagement and map control
- a broad-plane lane structure for flexible path manipulation
- minion waves driven by spawners controlled by the TD player
- resource acquisition and protection as a shared but asymmetric economy
- base destruction as the final objective

This concept is high-risk but promising because it creates a distinctive role split, a clear objective loop, and a map-control system that can evolve over time.

## 18. Summary

This game is built around a clear asymmetry: the TD player designs the battlefield, while the MOBA players execute on it. The main fantasy is not just building a tower defense, nor just fighting in a MOBA. It is creating a route, seeing the enemy react, and then turning that tactical setup into a dramatic push toward the enemy base.

The project is intentionally ambitious, but the current draft defines a strong and testable core: one TD player, several MOBA players, one broad plane, one resource loop, one enemy base objective, and a gameplay loop built around battlefield manipulation and direct combat execution.
