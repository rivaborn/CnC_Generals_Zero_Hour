# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/RadarUpgrade.cpp

## Purpose
Handles radar upgrade functionality for game objects, including adding/removing radar for players and managing upgrade state.

## Responsibilities
- Manages radar upgrades for game objects
- Handles radar addition/removal when objects are captured or deleted
- Extends radar range via RadarUpdate module
- Serializes upgrade state for network sync

## Key Types
- **RadarUpgradeModuleData (Class)**: Contains radar upgrade configuration (e.g., disable proof flag)
- **RadarUpgrade (Class)**: Implements radar upgrade logic for game objects

## Key Functions
### `buildFieldParse`
- Purpose: Registers INI field parsing for RadarUpgradeModuleData
- Calls: `UpgradeModuleData::buildFieldParse`

### `onDelete`
- Purpose: Removes radar from player when object is deleted
- Calls: `getObject()->isDisabled()`, `getObject()->getControllingPlayer()`, `Player::removeRadar`

### `onCapture`
- Purpose: Transfers radar ownership when object is captured
- Calls: `getObject()->isDisabled()`, `Player::removeRadar`, `Player::addRadar`

### `upgradeImplementation`
- Purpose: Applies radar upgrade to player and extends radar range
- Calls: `Player::addRadar`, `getObject()->findUpdateModule`, `RadarUpdate::extendRadar`

### `crc` and `xfer`
- Purpose: Network serialization for upgrade state
- Calls: `UpgradeModule::crc`, `UpgradeModule::xfer`

## Globals
- None

## Dependencies
- `UpgradeModule`, `Player`, `RadarUpdate`, `Xfer`, `MultiIniFieldParse`
- INI parsing utilities (`INI::parseBool`)
