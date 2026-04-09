# Generals/Code/GameEngine/Source/Common/RTS/ResourceGatheringManager.cpp

## Purpose
This file manages resource gathering operations in the game, tracking supply centers and warehouses and making decisions on where to gather resources from.

## Responsibilities
- Track supply centers and warehouses.
- Determine the best supply center or warehouse for a given object to gather resources from.
- Handle adding and removing supply centers and warehouses.
- Compute relative costs between objects for resource gathering decisions.

## Key Types
- None

## Key Functions
### computeRelativeCost
- Purpose: Computes the cost of moving an object to another object, considering various factors like distance and availability.
- Calls:
  - `TheActionManager->canTransferSuppliesAt`
  - `dockInterface->isClearToApproach`
  - `ThePartitionManager->getDistanceSquared`

### findBestSupplyWarehouse
- Purpose: Finds the best supply warehouse for a given object to gather resources from, considering distance and availability.
- Calls:
  - `computeRelativeCost`
  - `TheGameLogic->findObjectByID`

### findBestSupplyCenter
- Purpose: Finds the best supply center for a given object to gather resources from, considering distance and availability.
- Calls:
  - `computeRelativeCost`
  - `TheGameLogic->findObjectByID`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/ResourceGatheringManager.h"
  - "Common/ActionManager.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/SupplyTruckAIUpdate.h"
  - "GameLogic/Module/SupplyCenterDockUpdate.h"
  - "GameLogic/Module/SupplyWarehouseDockUpdate.h"
  - "GameLogic/Module/UpdateModule.h"

- External symbols used:
  - `TheActionManager`
  - `ThePartitionManager`
  - `TheGameLogic`
