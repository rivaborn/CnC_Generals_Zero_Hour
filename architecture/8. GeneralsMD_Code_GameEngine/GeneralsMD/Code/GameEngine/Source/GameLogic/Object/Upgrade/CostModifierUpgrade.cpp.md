# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/CostModifierUpgrade.cpp

## Purpose
Implements an upgrade module that modifies production costs by a percentage for specific object types.

## Responsibilities
- Applies cost percentage modifiers to player production costs
- Handles upgrade application, deletion, and capture events
- Manages serialization and network synchronization via Xfer
- Integrates with player cost modification system

## Key Types
- **CostModifierUpgradeModuleData (struct)**: Stores upgrade configuration (target object types and percentage)
- **CostModifierUpgrade (class)**: Upgrade module that applies cost modifiers

## Key Functions
### `CostModifierUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for upgrade module data
- Calls: `UpgradeModuleData::buildFieldParse`

### `CostModifierUpgrade::onDelete`
- Purpose: Removes cost modifiers when upgrade is deleted
- Calls: `getObject()->getControllingPlayer()`, `Player::removeKindOfProductionCostChange`

### `CostModifierUpgrade::onCapture`
- Purpose: Transfers cost modifiers between players during capture
- Calls: `Player::removeKindOfProductionCostChange`, `Player::addKindOfProductionCostChange`

### `CostModifierUpgrade::upgradeImplementation`
- Purpose: Applies the cost modifier when upgrade is executed
- Calls: `Player::addKindOfProductionCostChange`

### `CostModifierUpgrade::xfer`
- Purpose: Handles network serialization of upgrade state
- Calls: `UpgradeModule::xfer`, `Xfer::xferVersion`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/player.h`, `Common/Xfer.h`, `GameLogic/Module/CostModifierUpgrade.h`, `GameLogic/Object.h`, `Common/BitFlagsIO.h`
- `UpgradeModule`, `UpgradeModuleData`, `MultiIniFieldParse`, `KindOfMaskType`, `INI`, `Xfer`, `XferVersion`
