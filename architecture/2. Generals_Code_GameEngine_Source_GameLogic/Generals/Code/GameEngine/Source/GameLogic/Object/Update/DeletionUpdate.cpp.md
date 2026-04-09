# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DeletionUpdate.cpp

## Purpose
This file implements the `DeletionUpdate` class, which manages the countdown and destruction of game objects based on a specified lifetime.

## Responsibilities
- Manages the countdown timer for object deletion.
- Sets the wake frame for the update module.
- Calculates the sleep delay for the object's lifetime.
- Updates the object's geometry in debug mode.
- Destroys the object when its lifetime expires.

## Key Types
- `DeletionUpdate` (Class): Handles the countdown and destruction of game objects.
- None

## Key Functions
### DeletionUpdate::DeletionUpdate
- Purpose: Initializes the deletion update module with a specified lifetime range.
- Calls: 
  - `calcSleepDelay`
  - `setWakeFrame`

### DeletionUpdate::setLifetimeRange
- Purpose: Sets the minimum and maximum frames for the object's lifetime.
- Calls: 
  - `calcSleepDelay`
  - `setWakeFrame`

### DeletionUpdate::calcSleepDelay
- Purpose: Calculates a random delay within the specified range.
- Calls: 
  - `GameLogicRandomValue`

### DeletionUpdate::update
- Purpose: Updates the object's geometry and destroys it when its lifetime expires.
- Calls: 
  - `TheGameLogic->destroyObject`
  - `getObject`
  - `getGeometryInfo`
  - `setGeometryInfo`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/DeletionUpdate.h"
