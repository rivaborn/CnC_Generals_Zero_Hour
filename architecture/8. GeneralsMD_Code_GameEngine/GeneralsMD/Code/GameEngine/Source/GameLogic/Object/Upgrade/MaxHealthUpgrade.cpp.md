# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/MaxHealthUpgrade.cpp

## Purpose
Implements a module that modifies an object's maximum health value.

## Responsibilities
- Applies health upgrades to objects
- Handles health change types (e.g., relative to current health)
- Serializes/deserializes upgrade data
- Parses configuration from INI files

## Key Types
- **MaxHealthUpgradeModuleData (Class)**: Stores upgrade parameters (health amount and change type)
- **MaxHealthUpgrade (Class)**: Applies health upgrades to objects

## Key Functions
### `MaxHealthUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for upgrade data
- Calls: `UpgradeModuleData::buildFieldParse`

### `MaxHealthUpgrade::upgradeImplementation`
- Purpose: Applies the health upgrade to the object
- Calls: `getMaxHealthUpgradeModuleData`, `getObject`, `BodyModuleInterface::setMaxHealth`

### `MaxHealthUpgrade::crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `UpgradeModule::crc`

### `MaxHealthUpgrade::xfer`
- Purpose: Serializes/deserializes upgrade data
- Calls: `UpgradeModule::xfer`

### `MaxHealthUpgrade::loadPostProcess`
- Purpose: Post-load initialization
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Module/MaxHealthUpgrade.h`, `GameLogic/Module/BodyModule.h`
- `UpgradeModule`, `UpgradeModuleData`, `BodyModuleInterface`, `Xfer`, `MultiIniFieldParse`, `INI`
