# Generals/Code/GameEngine/Source/GameLogic/Object/Update/PowerPlantUpdate.cpp

## Purpose
Handles the update logic for power plants in the game, including extending and retracting rods.

## Responsibilities
- Manages the state of power plant rods (extended or retracted).
- Updates the visual condition of the power plant model.
- Handles serialization and deserialization of the module's state.

## Key Types
- PowerPlantUpdateModuleData (struct): Stores data related to power plant updates, such as rod extend time.
- PowerPlantUpdate (class): Manages the update logic for power plants.

## Key Functions
### extendRods
- Purpose: Extends or retracts the rods of a power plant.
- Calls:
  - `setModelConditionState`
  - `clearModelConditionFlags`
  - `setWakeFrame`

### update
- Purpose: Updates the power plant's state, setting it to extended and upgrading condition.
- Calls:
  - `clearAndSetModelConditionState`
  - `setWakeFrame`

### crc
- Purpose: Computes the CRC for the module.
- Calls:
  - `crc` (base class)

### xfer
- Purpose: Serializes or deserializes the module's state.
- Calls:
  - `xferVersion`
  - `xferBool`
  - `xfer` (base class)

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ModelState.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/PowerPlantUpdate.h"
