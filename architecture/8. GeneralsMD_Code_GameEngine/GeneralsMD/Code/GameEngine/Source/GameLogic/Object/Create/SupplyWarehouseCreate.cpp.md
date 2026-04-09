# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/SupplyWarehouseCreate.cpp

## Purpose
Handles creation logic for supply warehouses, updating resource managers for all players.

## Responsibilities
- Initializes supply warehouse creation module
- Notifies all players' resource managers when a warehouse is created
- Implements serialization (CRC, Xfer, loadPostProcess)

## Key Types
- SupplyWarehouseCreate (Class): Module for supply warehouse creation logic

## Key Functions
### SupplyWarehouseCreate::onCreate
- Purpose: Registers the warehouse with all players' resource managers
- Calls: ThePlayerList->getPlayerCount, ThePlayerList->getNthPlayer, Player::getResourceGatheringManager, ResourceGatheringManager::addSupplyWarehouse

### SupplyWarehouseCreate::crc
- Purpose: Serialization CRC handler
- Calls: CreateModule::crc

### SupplyWarehouseCreate::xfer
- Purpose: Serialization handler
- Calls: CreateModule::xfer

### SupplyWarehouseCreate::loadPostProcess
- Purpose: Post-load processing
- Calls: CreateModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Player.h
- Common/PlayerList.h
- Common/ResourceGatheringManager.h
- Common/Xfer.h
- GameLogic/Module/SupplyWarehouseCreate.h
