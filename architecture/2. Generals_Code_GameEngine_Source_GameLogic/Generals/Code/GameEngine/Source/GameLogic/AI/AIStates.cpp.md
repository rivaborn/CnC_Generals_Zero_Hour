# Generals/Code/GameEngine/Source/GameLogic/AI/AIStates.cpp

## Purpose
This file implements AI behavior states for units in Command & Conquer Generals, including attack, hunt, and face states.

## Responsibilities
- Define and manage AI state machines for unit behaviors.
- Implement logic for attacking targets, scanning for enemies, and facing directions.
- Handle serialization and deserialization of AI states.

## Key Types
- **AIAttackMoveStateMachine (Class)**: Manages attack move state transitions.
- **AIAttackThenIdleStateMachine (Class)**: Handles attack then idle behavior.
- **None**: No enums or structs defined in this file.

## Key Functions
### cannotPossiblyAttackObject
- Purpose: Determines if a unit can possibly attack an object.
- Calls: None

### isSamePosition
- Purpose: Compares two positions to check if they are logically equal.
- Calls: None

### findEnemyInContainer
- Purpose: Finds an enemy within a container.
- Calls: None

### killEnemiesInContainer
- Purpose: Kills enemies within a container.
- Calls: None

### outOfWeaponRangeObject
- Purpose: Checks if an object is out of weapon range.
- Calls: None

### wantToSquishTarget
- Purpose: Determines if a unit wants to squish a target.
- Calls: None

### outOfWeaponRangePosition
- Purpose: Checks if a position is out of weapon range.
- Calls: None

## Globals
- **IDLE_COUNTDOWN_DELAY (Int)**: Delay for idle countdown.

## Dependencies
- Key includes:
  - "Common/ActionManager.h"
  - "GameLogic/AIStateMachine.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/TurretAI.h"
  - "GameLogic/Weapon.h"
