# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ActiveShroudUpgrade.cpp

## Purpose
Implements an upgrade module that modifies an object's shroud range in the game.

## Responsibilities
- Manages shroud range upgrades for game objects
- Handles INI field parsing for upgrade data
- Applies shroud range changes to objects
- Supports serialization (Xfer) and CRC operations

## Key Types
- **ActiveShroudUpgradeModuleData (Class)**: Stores upgrade data including new shroud range value
- **ActiveShroudUpgrade (Class)**: Implements the shroud upgrade functionality

## Key Functions
### ActiveShroudUpgradeModuleData::buildFieldParse
- Purpose: Registers INI field parsing for shroud upgrade data
- Calls: `UpgradeModuleData::buildFieldParse`

### ActiveShroudUpgrade::upgradeImplementation
- Purpose: Applies the shroud range upgrade to the object
- Calls: `getObject()->setShroudRange`, `getObject()->handlePartitionCellMaintenance`

### ActiveShroudUpgrade::crc
- Purpose: Handles CRC calculation for serialization
- Calls: `UpgradeModule::crc`

### ActiveShroudUpgrade::xfer
- Purpose: Handles object serialization/deserialization
- Calls: `UpgradeModule::xfer`, `xfer->xferVersion`

## Globals
None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/ActiveShroudUpgrade.h`, `GameLogic/Object.h`
- `MultiIniFieldParse`, `INI`, `UpgradeModuleData`, `UpgradeModule`, `Thing`, `Xfer`, `XferVersion`
