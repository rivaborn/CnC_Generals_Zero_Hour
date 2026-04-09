# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AssistedTargetingUpdate.cpp

## Purpose
This file implements the `AssistedTargetingUpdate` module, which handles assisted targeting logic for game objects in Command & Conquer Generals.

## Responsibilities
- Parses configuration data for assisted targeting.
- Determines if an object is free to assist in attacks.
- Manages weapon locks and AI-assisted attacks.
- Creates feedback lasers for visual cues during attacks.

## Key Types
- `AssistedTargetingUpdateModuleData (struct)`: Stores configuration data for the module.
- `AssistedTargetingUpdate (class)`: Implements the assisted targeting update logic.

## Key Functions
### buildFieldParse
- Purpose: Sets up field parsing for configuration data.
- Calls: `UpdateModuleData::buildFieldParse`

### AssistedTargetingUpdate
- Purpose: Constructor for the `AssistedTargetingUpdate` class.
- Calls: `setWakeFrame`, `getObject`

### ~AssistedTargetingUpdate
- Purpose: Destructor for the `AssistedTargetingUpdate` class.

### isFreeToAssist
- Purpose: Checks if an object is ready to assist in attacks.
- Calls: `isAbleToAttack`, `getCurrentWeapon`, `getStatus`

### assistAttack
- Purpose: Handles the logic for assisting another object's attack.
- Calls: `setWeaponLock`, `aiAttackObject`, `makeFeedbackLaser`

### makeFeedbackLaser
- Purpose: Creates a feedback laser between two objects.
- Calls: `newObject`, `findClientUpdateModule`, `initLaser`

### update
- Purpose: Updates the module's state.
- Returns: `UPDATE_SLEEP_FOREVER`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/ThingFactory.h"
  - "Common/Xfer
