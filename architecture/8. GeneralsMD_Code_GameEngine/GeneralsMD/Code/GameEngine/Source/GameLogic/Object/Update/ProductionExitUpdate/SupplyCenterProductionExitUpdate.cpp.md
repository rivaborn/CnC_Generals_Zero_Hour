# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProductionExitUpdate/SupplyCenterProductionExitUpdate.cpp

## Purpose
Handles the spawning and initial behavior of units produced by supply centers, including positioning, pathfinding, and supply truck autopilot activation.

## Responsibilities
- Spawns produced units at the correct exit position relative to the supply center.
- Sets up initial pathfinding for exiting units.
- Activates supply truck autopilot for produced units.
- Manages temporary stealth grants for exiting units.
- Provides rally point calculation for production exits.

## Key Types
- `SupplyCenterProductionExitUpdate` (Class): Manages supply center production exits.
- `SupplyCenterProductionExitUpdateModuleData` (Struct): Contains module-specific data (not shown in this file).

## Key Functions
### `exitObjectViaDoor`
- Purpose: Spawns a new unit at the supply center's exit point and sets up its initial behavior.
- Calls: `getObject`, `getSupplyCenterProductionExitUpdateModuleData`, `TheTerrainLogic->getGroundHeight`, `TheAI->pathfinder()->addObjectToPathfindMap`, `ai->aiFollowExitProductionPath`, `supplyTruckAI->setForceWantingState`, `stealth->receiveGrant`.

### `getExitPosition`
- Purpose: Calculates the world-space exit position for units based on the supply center's model and orientation.
- Calls: `getObject`, `getSupplyCenterProductionExitUpdateModuleData`.

### `getNaturalRallyPoint`
- Purpose: Retrieves the natural rally point for production exits, optionally offset for pathfinding.
- Calls: `getSupplyCenterProductionExitUpdateModuleData`, `getObject`.

### `crc`
- Purpose: Serialization CRC calculation for network sync.
- Calls: `UpdateModule::crc`.

### `xfer`
- Purpose: Serialization method for saving/loading the module's state.
- Calls: `UpdateModule::xfer`.

### `loadPostProcess`
- Purpose: Post-processing after loading module data.
- Calls: `UpdateModule::loadPostProcess`.

## Globals
- `m_rallyPoint` (Coord3D): Stores the custom rally point if set.
- `m_rallyPointExists` (Bool): Flag indicating if a custom rally point is set.

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `Lib/BaseType.h`, `GameLogic/AI.h`, `GameLogic/AIPathfind.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/SupplyCenterProductionExitUpdate.h`, `GameLogic/Module/SupplyTruckAIUpdate.h`, `GameLogic
