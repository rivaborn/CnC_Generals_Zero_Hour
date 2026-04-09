# Generals/Code/GameEngine/Source/GameLogic/Object/Create/SupplyCenterCreate.cpp

## Purpose
Handles the creation and build completion of Supply Centers in the game, updating Resource Gathering Managers for all players.

## Responsibilities
- Manages the lifecycle of Supply Center objects.
- Updates Resource Gathering Managers when a Supply Center is built.
- Handles CRC (Cyclic Redundancy Check) and Xfer (transfer) operations for data integrity.

## Key Types
- `SupplyCenterCreate` (Class): Manages Supply Center creation logic.
- None

## Key Functions
### onCreate
- Purpose: Called when the object is created.
- Calls: None

### onBuildComplete
- Purpose: Updates Resource Gathering Managers for all players when a Supply Center build is complete.
- Calls:
  - `shouldDoOnBuildComplete`
  - `CreateModule::onBuildComplete`
  - `ThePlayerList->getPlayerCount`
  - `ThePlayerList->getNthPlayer`
  - `getResourceGatheringManager`
  - `addSupplyCenter`

### crc
- Purpose: Handles CRC operations for data integrity.
- Calls:
  - `CreateModule::crc`

### xfer
- Purpose: Handles Xfer (transfer) operations for data serialization/deserialization.
- Calls:
  - `xfer->xferVersion`
  - `CreateModule::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading.
- Calls:
  - `CreateModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/ResourceGatheringManager.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/SupplyCenterCreate.h"
