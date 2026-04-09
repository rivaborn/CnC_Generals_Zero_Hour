# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/SupplyWarehouseDockUpdate.cpp

## Purpose
Handles supply warehouse docking logic, managing supply boxes transfer between supply trucks and warehouses.

## Responsibilities
- Manages supply box inventory for warehouses
- Handles docking actions between supply trucks and warehouses
- Updates visual supply status for drawable objects
- Implements warehouse destruction when empty (configurable)
- Manages crippled dock behavior during attacks

## Key Types
- **SupplyWarehouseDockUpdateModuleData (Class)**: Stores module configuration (starting boxes, delete-when-empty flag)
- **SupplyWarehouseDockUpdate (Class)**: Main docking update logic handler
- **None**: No enums/structs defined

## Key Functions
### `action(Object* docker, Object *drone)`
- Purpose: Handles the actual docking action between supply truck and warehouse
- Calls: `getGeometryInfo()`, `ThePartitionManager->getDistanceSquared()`, `getAIUpdateInterface()->getSupplyTruckAIInterface()`, `gainOneBox()`, `TheGameLogic->destroyObject()`, `updateDrawableSupplyStatus()`

### `setCashValue(Int cashValue)`
- Purpose: Converts cash value to supply boxes and updates display
- Calls: `updateDrawableSupplyStatus()`

### `setDockCrippled(Bool setting)`
- Purpose: Handles warehouse destruction logic when crippled
- Calls: `TheGameLogic->findObjectByID()`, `kill()`, `aiIdle()`, `setForceWantingState()`

### `xfer(Xfer *xfer)`
- Purpose: Serialization for network sync
- Calls: `DockUpdate::xfer()`, `xferVersion()`, `xferInt()`

## Globals
- **None**: No global/static variables

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `Common/Xfer.h`, `GameClient/Drawable.h`
- `GameLogic/Module/SupplyWarehouseDockUpdate.h`, `GameLogic/Module/SupplyTruckAIUpdate.h`
- `GameLogic/Object.h`, `GameLogic/PartitionManager.h`, `GameLogic/AIPathfind.h`
- Uses `TheGameLogic`, `ThePartitionManager`, `TheGlobalData` global instances
