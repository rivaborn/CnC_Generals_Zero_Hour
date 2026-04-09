# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FloatUpdate.cpp

## Purpose
This file implements the `FloatUpdate` module, which handles the floating behavior of game objects on water surfaces.

## Responsibilities
- Manages the floating state of an object.
- Updates the object's position to stay on top of water.
- Applies rotational effects for visual movement.

## Key Types
- `FloatUpdateModuleData (struct)`: Stores configuration data for the float update module.
- `FloatUpdate (class)`: Implements the logic for floating objects.

## Key Functions
### FloatUpdate::update
- Purpose: Updates the object's position to stay on top of water and applies rotational effects.
- Calls:
  - `getObject()->getPosition()`
  - `TheTerrainLogic->isUnderwater()`
  - `getObject()->setPosition()`
  - `getObject()->getDrawable()`
  - `draw->setInstanceMatrix()`

### FloatUpdate::crc
- Purpose: Extends the base class CRC method.
- Calls:
  - `UpdateModule::crc()`

### FloatUpdate::xfer
- Purpose: Handles serialization and deserialization of the float update module data.
- Calls:
  - `xfer->xferVersion()`
  - `UpdateModule::xfer()`
  - `xfer->xferBool()`

### FloatUpdate::loadPostProcess
- Purpose: Extends the base class post-load processing.
- Calls:
  - `UpdateModule::loadPostProcess()`

## Globals
None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/Module/FloatUpdate.h"
  - "GameLogic/GameLogic.h"
  - "GameClient/Drawable.h"
