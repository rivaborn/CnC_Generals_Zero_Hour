# Generals/Code/GameEngine/Source/GameLogic/Object/Create/SupplyWarehouseCreate.cpp

## Purpose
This file contains the implementation for the `SupplyWarehouseCreate` class, which handles the creation logic of supply warehouses in the game. It updates resource gathering managers for all players when a supply center is created.

## Responsibilities
- Handles the creation of supply warehouses.
- Updates resource gathering managers for all players upon warehouse creation.
- Implements CRC and Xfer methods for data integrity and transfer.

## Key Types
- `SupplyWarehouseCreate (Class)`: Manages the creation logic of supply warehouses.

## Key Functions
### SupplyWarehouseCreate::onCreate
- Purpose: Updates resource gathering managers for all players when a supply center is created.
- Calls:
  - `ThePlayerList->getPlayerCount()`
  - `ThePlayerList->getNthPlayer()`
  - `currentPlayer->getResourceGatheringManager()`
  - `manager->addSupplyWarehouse()`

### SupplyWarehouseCreate::crc
- Purpose: Implements CRC method for data integrity.
- Calls:
  - `CreateModule::crc()`

### SupplyWarehouseCreate::xfer
- Purpose: Implements Xfer method for data transfer.
- Calls:
  - `xfer->xferVersion()`
  - `CreateModule::xfer()`

### SupplyWarehouseCreate::loadPostProcess
- Purpose: Implements load post process logic.
- Calls:
  - `CreateModule::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/ResourceGatheringManager.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/SupplyWarehouseCreate.h"
