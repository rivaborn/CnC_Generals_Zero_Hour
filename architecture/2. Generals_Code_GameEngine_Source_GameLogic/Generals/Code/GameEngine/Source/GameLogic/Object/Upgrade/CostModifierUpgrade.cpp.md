# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/CostModifierUpgrade.cpp

## Purpose
This file implements a cost modifier upgrade module for game objects in Command & Conquer Generals, modifying production costs by a specified percentage.

## Responsibilities
- Handles the creation and destruction of cost modifier upgrades.
- Manages the application and removal of cost modifications on object capture.
- Implements the upgrade logic to modify production costs for players.

## Key Types
- `CostModifierUpgradeModuleData (struct)`: Stores data for the cost modifier upgrade, including kind of effect and percentage.
- `CostModifierUpgrade (class)`: Represents the cost modifier upgrade module, handling its lifecycle and effects.

## Key Functions
### CostModifierUpgradeModuleData::buildFieldParse
- Purpose: Builds field parsing for the cost modifier upgrade module data.
- Calls: UpgradeModuleData::buildFieldParse

### CostModifierUpgrade::CostModifierUpgrade
- Purpose: Constructor for the cost modifier upgrade module.
- Calls: None

### CostModifierUpgrade::~CostModifierUpgrade
- Purpose: Destructor for the cost modifier upgrade module.
- Calls: None

### CostModifierUpgrade::onDelete
- Purpose: Handles cleanup when the upgrade is deleted.
- Calls: Player::removeKindOfProductionCostChange, UpgradeModule::setUpgradeExecuted

### CostModifierUpgrade::onCapture
- Purpose: Manages cost modifications on object capture.
- Calls: Player::removeKindOfProductionCostChange, Player::addKindOfProductionCostChange, UpgradeModule::setUpgradeExecuted

### CostModifierUpgrade::upgradeImplementation
- Purpose: Implements the upgrade logic to modify production costs.
- Calls: Player::addKindOfProductionCostChange

### CostModifierUpgrade::crc
- Purpose: Calculates the CRC for the cost modifier upgrade module.
- Calls: UpgradeModule::crc

### CostModifierUpgrade::xfer
- Purpose: Handles serialization and deserialization of the cost modifier upgrade module.
- Calls: Xfer::xferVersion, UpgradeModule::xfer

### CostModifierUpgrade::loadPostProcess
- Purpose: Performs post-load processing for the cost modifier upgrade module.
- Calls: UpgradeModule::loadPostProcess

## Globals
- None

## Dependencies
- `PreRTS.h`
- `Common/player.h`
- `Common/Xfer.h`
- `GameLogic/Module/CostModifierUpgrade.h`
- `GameLogic/Object.h`
- `Common/BitFlagsIO.h`
