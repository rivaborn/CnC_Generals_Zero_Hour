# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FireSpreadUpdate.cpp

## Purpose
This file implements the `FireSpreadUpdate` module, which handles the logic for spreading fire among objects in the game. It checks if an object is on fire and attempts to ignite nearby flammable objects within a specified range.

## Responsibilities
- Detects when an object is on fire.
- Finds nearby flammable objects using a partition filter.
- Attempts to ignite these objects.
- Manages the delay between spread attempts.

## Key Types
- **PartitionFilterFlammable (Class)**: Filters objects to find those that are flammable and can be ignited.

## Key Functions
### FireSpreadUpdate::update
- Purpose: Updates the fire spreading logic for an object.
- Calls:
  - `ObjectCreationList::create`
  - `ThePartitionManager->getClosestObject`
  - `FlammableUpdate::tryToIgnite`
  - `UPDATE_SLEEP(calcNextSpreadDelay)`

### FireSpreadUpdate::startFireSpreading
- Purpose: Starts the fire spreading process for an object.
- Calls:
  - `setWakeFrame`

### FireSpreadUpdate::calcNextSpreadDelay
- Purpose: Calculates the next delay before attempting to spread fire again.
- Calls:
  - `GameLogicRandomValue`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/ObjectCreationList.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/FireSpreadUpdate.h"
  - "GameLogic/Module/FlammableUpdate.h"

- External symbols used:
  - `ThePartitionManager`
  - `OBJECT_STATUS_AFLAME`
  - `UPDATE_SLEEP_FOREVER`
  - `UPDATE_SLEEP`
