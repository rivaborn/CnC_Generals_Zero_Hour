# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/UnpauseSpecialPowerUpgrade.cpp

## Purpose
Handles an upgrade that unpauses a special power's timer when applied.

## Responsibilities
- Manages unpausing of special power countdowns
- Parses configuration for special power template references
- Implements upgrade logic and serialization

## Key Types
- `UnpauseSpecialPowerUpgradeModuleData` (Class): Holds data for the upgrade, including special power template reference
- `UnpauseSpecialPowerUpgrade` (Class): Upgrade module that unpauses special powers

## Key Functions
### `upgradeImplementation`
- Purpose: Unpauses the countdown for the specified special power
- Calls: `getObject`, `getBehaviorModules`, `getSpecialPower`, `getSpecialPowerTemplate`, `pauseCountdown`

### `buildFieldParse`
- Purpose: Defines INI field parsing for the module data
- Calls: `UpgradeModuleData::buildFieldParse`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `UpgradeModule::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `UpgradeModule::xfer`

### `loadPostProcess`
- Purpose: Post-load processing
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/SpecialPower.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/SpecialPowerModule.h`, `GameLogic/Module/UnpauseSpecialPowerUpgrade.h`
- `MultiIniFieldParse`, `INI`, `Thing`, `BehaviorModule`, `SpecialPowerModuleInterface`, `UpgradeModule`, `Xfer`, `XferVersion`
