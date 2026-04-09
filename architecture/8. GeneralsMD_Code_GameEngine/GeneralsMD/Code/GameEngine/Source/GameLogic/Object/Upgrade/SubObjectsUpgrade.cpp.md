# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/SubObjectsUpgrade.cpp

## Purpose
Handles showing/hiding subobjects on game objects based on upgrade states, overriding animation subobject states.

## Responsibilities
- Parses INI fields for show/hide subobject lists
- Applies subobject visibility changes when upgrades are activated
- Checks for conflicting upgrades before applying changes
- Serializes/deserializes upgrade data

## Key Types
- **SubObjectsUpgradeModuleData (Class)**: Holds configuration for which subobjects to show/hide
- **SubObjectsUpgrade (Class)**: Module that manages subobject visibility based on upgrades

## Key Functions
### `SubObjectsUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for show/hide subobject lists
- Calls: `UpgradeModuleData::buildFieldParse`

### `SubObjectsUpgrade::upgradeImplementation`
- Purpose: Applies subobject visibility changes when upgrade is activated
- Calls: `getUpgradeActivationMasks`, `getObject`, `getControllingPlayer`, `showSubObject`, `updateSubObjects`

### `SubObjectsUpgrade::crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `UpgradeModule::crc`

### `SubObjectsUpgrade::xfer`
- Purpose: Serializes/deserializes upgrade data
- Calls: `UpgradeModule::xfer`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/Object.h`, `GameLogic/Module/SubObjectsUpgrade.h`
