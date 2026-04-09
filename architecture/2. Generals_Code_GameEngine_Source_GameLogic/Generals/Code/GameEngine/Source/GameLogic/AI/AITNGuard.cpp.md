# Generals/Code/GameEngine/Source/GameLogic/AI/AITNGuard.cpp

## Purpose
This file contains the implementation of AI logic for guard units in Command & Conquer Generals, including state machines and functions to handle tunnel networks and enemy detection.

## Responsibilities
- Manage guard states for AI-controlled units.
- Detect and respond to attacks on guarded units.
- Navigate through tunnel networks.
- Scan for enemies within vision range.

## Key Types
- **AITNGuardMachine (StateMachine)**: Manages the guard state machine for a unit.
- **AITNGuardInnerState, AITNGuardOuterState, etc. (State)**: Different states within the guard state machine.
- **TunnelNetworkExitConditions**: Conditions to exit tunnel network states.

## Key Functions
### hasAttackedMeAndICanReturnFire
- Purpose: Determines if a unit can return fire after being attacked.
- Calls: `getBodyModule`, `getClearableLastAttacker`, `findObjectByID`, `getAbleToAttackSpecificObject`.

### findBestTunnel
- Purpose: Finds the best tunnel for a unit to enter based on proximity.
- Calls: `getTunnelSystem`, `getContainerList`, `findObjectByID`.

### TunnelNetworkScan
- Purpose: Scans for enemies within the vision range of a unit.
- Calls: `getClosestObject` with various filters.

## Globals
- **CLOSE_ENOUGH (Real)**: A constant representing a close enough distance threshold.

## Dependencies
- Key includes:
  - "Common/PerfTimer.h"
  - "Common/Team.h"
  - "GameLogic/AI.h"
  - "GameLogic/AITNGuard.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
