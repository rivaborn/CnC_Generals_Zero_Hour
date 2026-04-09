# GeneralsMD/Code/GameEngine/Source/Common/RTS/ResourceGatheringManager.cpp

## Purpose
Manages resource gathering logic for supply trucks, tracking supply centers and warehouses, and determining optimal docking targets.

## Responsibilities
- Maintains lists of supply centers and warehouses
- Finds best docking targets for supply trucks
- Computes relative costs for pathfinding decisions
- Handles object lifecycle (add/remove) for supply structures

## Key Types
- ResourceGatheringManager (Class): Manages supply truck resource gathering logic
- computeRelativeCost (Function): Calculates cost/distance for supply truck docking

## Key Functions
### computeRelativeCost
- Purpose: Calculates relative cost/distance for supply truck to dock at target
- Calls: TheActionManager->canTransferSuppliesAt, destObject->getDockUpdateInterface, ThePartitionManager->getDistanceSquared

### findBestSupplyWarehouse
- Purpose: Finds optimal supply warehouse for a supply truck
- Calls: queryObject->getAI, supplyTruckAI->getPreferredDockID, TheGameLogic->findObjectByID, computeRelativeCost

### findBestSupplyCenter
- Purpose: Finds optimal supply center for a supply truck
- Calls: queryObject->getAI, supplyTruckAI->getPreferredDockID, TheGameLogic->findObjectByID, computeRelativeCost

## Globals
- None

## Dependencies
- PreRTS.h, ResourceGatheringManager.h, ActionManager.h, Xfer.h, GameLogic.h, Object.h, PartitionManager.h
- SupplyTruckAIUpdate.h, SupplyCenterDockUpdate.h, SupplyWarehouseDockUpdate.h, UpdateModule.h
- TheActionManager, TheGameLogic, ThePartitionManager (global instances)
