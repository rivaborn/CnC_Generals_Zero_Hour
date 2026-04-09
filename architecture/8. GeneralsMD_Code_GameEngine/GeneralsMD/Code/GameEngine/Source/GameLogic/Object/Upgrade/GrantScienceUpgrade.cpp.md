# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/GrantScienceUpgrade.cpp

## Purpose
Implements a game module that grants a specified science type to a player once upgrade requirements are met.

## Responsibilities
- Parses configuration data for science grant upgrades
- Manages science type granting logic
- Handles serialization (Xfer) and CRC for network sync
- Extends base UpgradeModule functionality

## Key Types
- **GrantScienceUpgradeModuleData (Class)**: Holds configuration for science grant upgrades
- **GrantScienceUpgrade (Class)**: Module that grants science when upgrade completes

## Key Functions
### `buildFieldParse`
- Purpose: Registers INI field parsers for GrantScienceUpgradeModuleData
- Calls: `UpgradeModuleData::buildFieldParse`

### `upgradeImplementation`
- Purpose: Grants specified science to controlling player when upgrade completes
- Calls: `TheScienceStore->getScienceFromInternalName`, `player->grantScience`

### `crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `UpgradeModule::crc`

### `xfer`
- Purpose: Serializes/deserializes module state for network sync
- Calls: `UpgradeModule::xfer`

### `loadPostProcess`
- Purpose: Post-processing after module loading
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- **TheScienceStore (External)**: Global science store reference

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/GrantScienceUpgrade.h`
- `INI` namespace, `UpgradeModule`, `UpgradeModuleData`, `Thing`, `Object`, `Player`, `Xfer`, `XferVersion`
