# Generals/Code/GameEngine/Source/GameLogic/Object/Update/PilotFindVehicleUpdate.cpp

## Purpose
This file contains the implementation of the `PilotFindVehicleUpdate` class, which is an update module responsible for handling the AI behavior of finding and targeting vehicles within a specified range.

## Responsibilities
- Manages the scanning process to find nearby vehicles.
- Handles AI movement to bases if no suitable targets are found.
- Ensures that only idle AI units perform these actions.

## Key Types
- `PilotFindVehicleUpdateModuleData (struct)`: Stores configuration data for the update module, such as scan rate, range, and minimum health threshold.
- `PilotFindVehicleUpdate (class)`: Implements the logic for finding and targeting vehicles by AI-controlled objects.

## Key Functions
### PilotFindVehicleUpdate::update()
- Purpose: The main update function that checks if the AI unit is idle and scans for nearby vehicles. If no suitable target is found, it moves the unit to a base.
- Calls:
  - `getObject()`
  - `getControllingPlayer()->getPlayerType()`
  - `isIdle()`
  - `aiEnter()`
  - `aiMoveToPosition()`
  - `scanClosestTarget()`

### PilotFindVehicleUpdate::scanClosestTarget()
- Purpose: Scans for the closest target vehicle within the specified range that meets health criteria and collision preferences.
- Calls:
  - `getPosition()`
  - `getBodyModule()->getHealth()`
  - `getBodyModule()->getMaxHealth()`
  - `wouldLikeToCollideWith()`

## Globals
- None

## Dependencies
- Key includes:
  - "GameClient\Drawable.h"
  - "Common/ActionManager.h"
  - "Common/Player.h"
  - "Common/RandomValue.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameLogic\GameLogic.h"
  - "GameLogic\PartitionManager.h"
  - "GameLogic\Object.h"
  - "GameLogic\ObjectIter.h"
  - "GameLogic\Module\PilotFindVehicleUpdate.h"
  - "GameLogic\Module\AIUpdate.h"
  - "GameLogic\Module\CollideModule.h"
