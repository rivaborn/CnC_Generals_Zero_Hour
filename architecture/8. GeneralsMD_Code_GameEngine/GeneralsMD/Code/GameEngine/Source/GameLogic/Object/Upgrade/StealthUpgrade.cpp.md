# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/StealthUpgrade.cpp

## Purpose
Implements a game module that grants stealth capability to an object and its spawns.

## Responsibilities
- Grants `OBJECT_STATUS_CAN_STEALTH` status to the owner object
- Propagates stealth upgrade to spawned units if applicable
- Handles serialization (Xfer) and CRC for save/load
- Manages module lifecycle (construction, destruction, post-load)

## Key Types
- **StealthUpgrade (Class)**: Module that applies stealth status to an object
- **UpgradeModule (Class)**: Base class for upgrade modules

## Key Functions
### `StealthUpgrade::upgradeImplementation`
- Purpose: Applies stealth status to the owner and its spawns
- Calls: `getObject()`, `setStatus()`, `isKindOf()`, `getSpawnBehaviorInterface()`, `giveSlavesStealthUpgrade()`

### `StealthUpgrade::crc`
- Purpose: Serializes module data for CRC calculation
- Calls: `UpgradeModule::crc()`

### `StealthUpgrade::xfer`
- Purpose: Serializes module data for save/load
- Calls: `UpgradeModule::xfer()`

### `StealthUpgrade::loadPostProcess`
- Purpose: Post-load initialization
- Calls: `UpgradeModule::loadPostProcess()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/StealthUpgrade.h`, `GameLogic/Module/SpawnBehavior.h`, `GameLogic/Object.h`
- `Xfer`, `ModuleData`, `Thing`, `Object`, `SpawnBehaviorInterface`
