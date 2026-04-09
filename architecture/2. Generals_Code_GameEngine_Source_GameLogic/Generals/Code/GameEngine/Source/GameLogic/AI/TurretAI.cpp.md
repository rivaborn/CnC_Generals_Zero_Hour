# Generals/Code/GameEngine/Source/GameLogic/AI/TurretAI.cpp

## Purpose
This file implements the AI behavior for turrets in Command & Conquer Generals, including state management, target acquisition, and firing logic.

## Responsibilities
- Manage turret states such as idle, aim, fire, recenter, and hold.
- Handle turret rotation and pitch adjustments.
- Parse configuration data from INI files.
- Implement logic for sweeping and targeting enemies.

## Key Types
- **TurretStateMachine (Class)**: Manages the state transitions of a turret.
- **TurretAIData (Struct)**: Stores configuration data for turrets.
- **TurretAI (Class)**: Represents the AI logic for a single turret.

## Key Functions
### frameToSleepTime
- Purpose: Calculate sleep time based on given frames.
- Calls: `TheGameLogic->getFrame()`

### parseTWS
- Purpose: Parse weapon slot types from INI files.
- Calls: `INI::scanIndexList`, `INI::getNextToken`

## Globals
- **WAIT_INDEFINITELY (UnsignedInt)**: Represents an indefinite wait time.

## Dependencies
- Key includes:
  - "Common/GameAudio.h"
  - "GameLogic/TurretAI.h"
  - "GameLogic/WeaponSet.h"
- External symbols used:
  - `TheGameLogic`
  - `ThePartitionManager`
  - `TheWeaponSlotTypeNames`
