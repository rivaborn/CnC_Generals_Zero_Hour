# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FloatUpdate.cpp

## Purpose
Implements floating behavior for objects in the game, making them follow water surface height and apply gentle rocking motion.

## Responsibilities
- Adjusts object position to match water surface height
- Applies periodic yaw/pitch rotation for floating animation
- Handles serialization and CRC for network sync
- Manages enabled/disabled state via INI configuration

## Key Types
- **FloatUpdateModuleData (Class)**: Holds module configuration (enabled flag)
- **FloatUpdate (Class)**: Update module that implements floating logic

## Key Functions
### FloatUpdate::update
- Purpose: Updates object position and rotation to simulate floating
- Calls: `getObject()`, `getPosition()`, `TheTerrainLogic->isUnderwater()`, `setPosition()`, `getDrawable()`, `getInstanceMatrix()`, `setInstanceMatrix()`

### FloatUpdate::xfer
- Purpose: Serializes/deserializes module state for network sync
- Calls: `UpdateModule::xfer()`, `xferVersion()`, `xferBool()`

### FloatUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: `UpdateModuleData::buildFieldParse()`, `add()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/TerrainLogic.h`, `GameLogic/Module/FloatUpdate.h`, `GameLogic/GameLogic.h`, `GameClient/Drawable.h`
