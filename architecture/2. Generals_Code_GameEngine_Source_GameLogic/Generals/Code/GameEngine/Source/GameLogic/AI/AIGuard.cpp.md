# Generals/Code/GameEngine/Source/GameLogic/AI/AIGuard.cpp

## Purpose
This file implements the AI guard logic for units in Command & Conquer Generals, handling states like returning to a position, idling, attacking aggressors, and picking up crates.

## Responsibilities
- Manages guard states for AI-controlled units.
- Handles transitions between different guard states based on conditions.
- Implements logic for detecting enemies and initiating attacks.
- Coordinates unit movement and actions within the game environment.

## Key Types
- **AIGuardMachine (Class)**: Manages the overall guard behavior of a unit.
- **ExitConditions (Struct)**: Defines conditions under which a state should exit.
- **StateConditionInfo (Struct)**: Holds information about state transition conditions.

## Key Functions
### hasAttackedMeAndICanReturnFire
- Purpose: Determines if an AI unit can return fire to an attacker.
- Calls:
  - `getMachineOwner()`
  - `getBodyModule()`
  - `findObjectByID()`
  - `isAbleToAttackSpecificObject()`

## Globals
- **CLOSE_ENOUGH (Real)**: A constant representing a close enough distance for AI unit actions.

## Dependencies
- Key includes:
  - "Common/PerfTimer.h"
  - "Common/Team.h"
  - "Common/Xfer.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/AIGuard.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/CollideModule.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/PolygonTrigger.h"
