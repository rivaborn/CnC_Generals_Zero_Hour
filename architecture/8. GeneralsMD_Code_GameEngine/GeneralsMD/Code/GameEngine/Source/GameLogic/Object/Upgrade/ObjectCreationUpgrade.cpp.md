# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ObjectCreationUpgrade.cpp

## Purpose
Implements upgrades that spawn objects via Object Creation Lists (OCLs).

## Responsibilities
- Manages ObjectCreationUpgradeModuleData for parsing OCLs
- Handles object creation when upgrade is applied
- Provides serialization (Xfer) and CRC support
- Extends base UpgradeModule functionality

## Key Types
- **ObjectCreationUpgradeModuleData (Class)**: Holds OCL reference for upgrades
- **ObjectCreationUpgrade (Class)**: Upgrade module that spawns objects

## Key Functions
### `ObjectCreationUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for OCL data
- Calls: `UpgradeModuleData::buildFieldParse`

### `ObjectCreationUpgrade::upgradeImplementation`
- Purpose: Spawns objects defined in the OCL when upgrade is applied
- Calls: `ObjectCreationList::create`

### `ObjectCreationUpgrade::xfer`
- Purpose: Serializes upgrade data for network sync
- Calls: `UpgradeModule::xfer`, `xfer->xferVersion`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/ModelState.h`, `Common/Player.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameLogic/Module/ObjectCreationUpgrade.h`
- `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`
- `UpgradeModule`, `UpgradeModuleData`, `MultiIniFieldParse`, `INI`
