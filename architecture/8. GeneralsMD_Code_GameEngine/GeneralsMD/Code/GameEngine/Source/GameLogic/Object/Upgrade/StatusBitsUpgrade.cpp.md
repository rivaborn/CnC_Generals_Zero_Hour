# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/StatusBitsUpgrade.cpp

## Purpose
Implements a game upgrade module that modifies object status flags.

## Responsibilities
- Parses INI fields for status bits to set/clear
- Applies status bit changes to an object during upgrade
- Handles serialization (Xfer) and CRC for network sync
- Provides load-time post-processing

## Key Types
- **StatusBitsUpgradeModuleData (Class)**: Holds parsed INI data for status bits
- **StatusBitsUpgrade (Class)**: Upgrade module that modifies object status flags

## Key Functions
### `StatusBitsUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for status bit configuration
- Calls: `UpgradeModuleData::buildFieldParse`

### `StatusBitsUpgrade::upgradeImplementation`
- Purpose: Applies status bit changes to the target object
- Calls: `Object::setStatus`, `Object::clearStatus`

### `StatusBitsUpgrade::crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `UpgradeModule::crc`

### `StatusBitsUpgrade::xfer`
- Purpose: Serializes/deserializes upgrade module state
- Calls: `UpgradeModule::xfer`

### `StatusBitsUpgrade::loadPostProcess`
- Purpose: Performs post-load initialization
- Calls: `UpgradeModule::loadPostProcess`

## Globals
None

## Dependencies
- `PreRTS.h`, `Xfer.h`, `Drawable.h`, `Object.h`, `StatusBitsUpgrade.h`
- `MultiIniFieldParse`, `ObjectStatusMaskType`, `UpgradeModuleData`, `UpgradeModule`, `Xfer`, `XferVersion`
