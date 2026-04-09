# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CostModifierUpgrade.h

## Purpose
Defines a game module that modifies the cost of objects when applied as an upgrade.

## Responsibilities
- Provides data structure for cost modifier upgrades
- Implements upgrade logic that applies percentage cost modifications
- Handles object deletion and capture events for upgrades
- Manages module lifecycle and memory allocation

## Key Types
- **CostModifierUpgradeModuleData (Class)**: Stores upgrade data including percentage and kind-of mask
- **CostModifierUpgrade (Class)**: Implements the upgrade module behavior
- **CostModifierUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CostModifierUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### CostModifierUpgradeModuleData::buildFieldParse
- Purpose: Parses configuration data for the module
- Calls: Not inferable

### CostModifierUpgrade::upgradeImplementation
- Purpose: Applies the cost modification upgrade
- Calls: Not inferable

### CostModifierUpgrade::onDelete
- Purpose: Handles cleanup when the upgrade is deleted
- Calls: Not inferable

### CostModifierUpgrade::onCapture
- Purpose: Handles ownership transfer of the upgrade
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `Common/KindOf.h` (for KindOfMaskType)
- `Thing` (forward reference)
- `Player` (forward reference)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool management macros
