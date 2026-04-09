# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FireOCLAfterWeaponCooldownUpdate.cpp

## Purpose
This file implements a module that tracks an object's firing status and creates an Object Creation List (OCL) after the object stops firing, meeting certain conditions.

## Responsibilities
- Tracks weapon usage and cooldown.
- Creates OCL when specified conditions are met.
- Handles upgrades and validity checks.

## Key Types
- `FireOCLAfterWeaponCooldownUpdateModuleData` (struct): Stores configuration data for the module.
- `FireOCLAfterWeaponCooldownUpdate` (class): Implements the update logic for the module.

## Key Functions
### FireOCLAfterWeaponCooldownUpdate::update
- Purpose: Updates the module's state and checks conditions to create an OCL.
- Calls:
  - `getUpgradeActivationMasks`
  - `testUpgradeConditions`
  - `fireOCL`
  - `resetStats`

### FireOCLAfterWeaponCooldownUpdate::fireOCL
- Purpose: Creates an OCL based on the weapon's firing duration and configuration.
- Calls:
  - `ObjectCreationList::create`
  - `resetStats`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Weaponset.h"
  - "GameLogic/Module/FireOCLAfterWeaponCooldownUpdate.h"

- External symbols used:
  - `TheGameLogic`
  - `SECONDS_PER_LOGICFRAME_REAL`
  - `LOGICFRAMES_PER_SECOND`
