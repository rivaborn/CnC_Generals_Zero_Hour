# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/SupplyWarehouseDockUpdate.cpp

## Purpose
This file contains the implementation for `SupplyWarehouseDockUpdate`, which manages supply dock interactions in the game, including handling supply transactions and updating visual representations.

## Responsibilities
- Manages supply transactions between docks and supply trucks.
- Updates the visual status of supply boxes.
- Handles docking actions, ensuring proximity checks and box transfers.
- Manages the lifecycle of supply docks, including deletion when empty.

## Key Types
- `SupplyWarehouseDockUpdateModuleData (struct)`: Stores configuration data for supply dock updates.
- `SupplyWarehouseDockUpdate (class)`: Implements the logic for supply dock interactions.

## Key Functions
### SupplyWarehouseDockUpdate::action
- Purpose: Handles the action of a supply truck docking, transferring boxes and updating status.
- Calls:
  - `ThePartitionManager->getDistanceSquared`
  - `docker->setPosition`
  - `ai->gainOneBox`
  - `TheGameLogic->destroyObject`
  - `draw->updateDrawableSupplyStatus`

### SupplyWarehouseDockUpdate::setDockCrippled
- Purpose: Sets the dock's crippled state, potentially killing or disabling active dockers.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `victim->kill`
  - `supplyTruckAI->setForceWantingState`

### SupplyWarehouseDockUpdate::setCashValue
- Purpose: Updates the number of boxes based on a cash value input.
- Calls:
  - `draw->updateDrawableSupplyStatus`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/GlobalData.h`
  - `Common/Xfer.h`
  - `GameClient/Drawable.h`
  - `GameLogic/Module/SupplyWarehouseDockUpdate.h`
  - `GameLogic/Module/SupplyTruckAIUpdate.h`
  - `GameLogic/Object.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/AIPathfind.h`
