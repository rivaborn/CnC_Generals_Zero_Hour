# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/SupplyCenterCreate.cpp

## Purpose
Handles creation logic for Supply Center objects in the game, updating resource management systems when a Supply Center is built.

## Responsibilities
- Initializes Supply Center creation module
- Updates player resource managers when a Supply Center is completed
- Manages serialization/deserialization for network sync
- Handles post-load processing

## Key Types
- SupplyCenterCreate (Class): Module for Supply Center creation logic
- CreateModule (Class): Base class for creation modules

## Key Functions
### SupplyCenterCreate::onBuildComplete
- Purpose: Notifies all players' resource managers about the new Supply Center
- Calls: CreateModule::onBuildComplete, ThePlayerList->getNthPlayer, Player::getResourceGatheringManager, ResourceGatheringManager::addSupplyCenter

### SupplyCenterCreate::crc
- Purpose: Serializes/deserializes CRC data for network sync
- Calls: CreateModule::crc

### SupplyCenterCreate::xfer
- Purpose: Handles versioned serialization for network sync
- Calls: CreateModule::xfer

### SupplyCenterCreate::loadPostProcess
- Purpose: Performs post-load initialization
- Calls: CreateModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Player.h
- Common/PlayerList.h
- Common/ResourceGatheringManager.h
- Common/Xfer.h
- GameLogic/Module/SupplyCenterCreate.h
- ThePlayerList (external)
