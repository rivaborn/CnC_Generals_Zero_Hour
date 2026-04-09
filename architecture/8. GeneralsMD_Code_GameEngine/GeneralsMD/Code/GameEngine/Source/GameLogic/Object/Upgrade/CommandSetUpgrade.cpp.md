# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/CommandSetUpgrade.cpp

## Purpose
Handles an upgrade module that changes an object's command set based on configuration and player/object upgrade state.

## Responsibilities
- Parses INI fields for command set overrides
- Applies command set changes based on upgrade conditions
- Refreshes UI when command sets change
- Serializes/deserializes upgrade state

## Key Types
- **CommandSetUpgradeModuleData (Class)**: Holds parsed INI data for command set overrides
- **CommandSetUpgrade (Class)**: Upgrade module that applies command set changes

## Key Functions
### `CommandSetUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for command set upgrade data
- Calls: `UpgradeModuleData::buildFieldParse`

### `CommandSetUpgrade::upgradeImplementation`
- Purpose: Applies the appropriate command set override based on upgrade conditions
- Calls: `TheUpgradeCenter->findUpgrade`, `obj->getControllingPlayer`, `player->getCompletedUpgradeMask`, `obj->getObjectCompletedUpgradeMask`, `obj->setCommandSetStringOverride`, `TheControlBar->markUIDirty`

### `CommandSetUpgrade::crc`
- Purpose: Computes CRC for network synchronization
- Calls: `UpgradeModule::crc`

### `CommandSetUpgrade::xfer`
- Purpose: Serializes/deserializes upgrade state
- Calls: `UpgradeModule::xfer`

### `CommandSetUpgrade::loadPostProcess`
- Purpose: Post-load initialization
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `Common/Player.h`, `GameClient/ControlBar.h`, `GameLogic/Module/CommandSetUpgrade.h`, `GameLogic
