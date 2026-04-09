# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PilotFindVehicleUpdate.cpp

## Purpose
Handles AI behavior for pilots to find and board vehicles in need of repair.

## Responsibilities
- Scans for nearby vehicles needing repair
- Directs AI to move to vehicles or base when idle
- Manages periodic scanning with configurable parameters
- Filters targets by health, ownership, and collision compatibility

## Key Types
- **PilotFindVehicleUpdateModuleData (Class)**: Stores configuration for scan rate, range, and health threshold
- **PilotFindVehicleUpdate (Class)**: Main update module implementing the pilot behavior

## Key Functions
### `update()`
- Purpose: Main update loop that triggers scanning and AI actions
- Calls: `getObject()`, `getControllingPlayer()`, `getAI()`, `isIdle()`, `scanClosestTarget()`, `aiEnter()`, `aiMoveToPosition()`, `getAiBaseCenter()`

### `scanClosestTarget()`
- Purpose: Finds the closest valid vehicle target for boarding
- Calls: `ThePartitionManager->iterateObjectsInRange()`, `getBodyModule()`, `getHealth()`, `getMaxHealth()`, `getBehaviorModules()`, `getCollide()`, `wouldLikeToCollideWith()`

### `crc()`, `xfer()`, `loadPostProcess()`
- Purpose: Serialization and network synchronization methods
- Calls: `UpdateModule::crc()`, `UpdateModule::xfer()`, `UpdateModule::loadPostProcess()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `GameClient/Drawable.h`, `Common/ActionManager.h`, `Common/Player.h`, `Common/RandomValue.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/PartitionManager.h`, `GameLogic/Object.h`, `GameLogic/ObjectIter.h`, `GameLogic/Module/PilotFindVehicleUpdate.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/CollideModule.h`
