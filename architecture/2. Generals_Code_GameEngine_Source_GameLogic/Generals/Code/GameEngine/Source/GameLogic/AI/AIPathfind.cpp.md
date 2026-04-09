# Generals/Code/GameEngine/Source/GameLogic/AI/AIPathfind.cpp

## Purpose
This file implements the AI pathfinding system for Command & Conquer Generals, handling various pathfinding algorithms and optimizations.

## Responsibilities
- Pathfinding logic for units to navigate the game map.
- Optimization of paths for efficiency and effectiveness.
- Handling different movement types and constraints (e.g., water, ground).
- Debugging and visualization tools for pathfinding processes.

## Key Types
- **TCheckMovementInfo (Class)**: Stores information about movement checks, including cell coordinates, layer, radius, and surface types.
- **PathNode (Class)**: Represents a node in the pathfinding graph, with methods to manage connections and direction vectors.
- **Path (Class)**: Manages a sequence of PathNodes, providing methods for appending, prepending, and optimizing paths.

## Key Functions
### findAttackPath
- Purpose: Finds a path for an attacker to reach a target while considering line of sight and attack range.
- Calls: `isAttackViewBlockedByObstacle`, `buildActualPath`, `examineNeighboringCells`.

### findSafePath
- Purpose: Finds a safe path for a unit to move away from repulsor fields, avoiding dangerous areas.
- Calls: `getRadiusAndCenter`, `worldToCell`, `adjustCoordToCell`, `checkDestination`, `buildActualPath`, `examineNeighboringCells`.

## Globals
- **frameToShowObstacles (Int)**: Controls the display of obstacles during debugging.

## Dependencies
- Key includes:
  - "GameLogic/AIPathfind.h"
  - "Common/PerfTimer.h"
  - "Common/Player.h"
  - "GameLogic/AI.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"
