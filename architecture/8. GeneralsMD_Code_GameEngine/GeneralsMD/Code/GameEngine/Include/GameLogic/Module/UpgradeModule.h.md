# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UpgradeModule.h

## Purpose
Defines the UpgradeModule system for handling player upgrades in the game, including activation, conflicts, and effects.

## Responsibilities
- Manages upgrade state and execution
- Handles upgrade activation, conflicts, and removal
- Provides interface for upgrade-related behavior
- Integrates with FXList for visual effects

## Key Types
- **Player (Class)**: Not inferable.
- **UpgradeModuleInterface (Class)**: Abstract interface for upgrade modules.
- **UpgradeMuxData (Class)**: Data container for upgrade configuration (triggers, conflicts, FX).
- **UpgradeMux (Class)**: Mix-in class implementing core upgrade logic.
- **UpgradeModuleData (Struct)**: Module data for UpgradeModule.
- **UpgradeModule (Class)**: Concrete module implementing upgrade behavior.
- **UpgradeModuleMagicEnum (Enum)**: Not inferable.
- **UpgradeModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### `UpgradeMuxData::getUpgradeActivationMasks`
- Purpose: Computes activation and conflicting upgrade masks.
- Calls: None visible.

### `UpgradeMuxData::performUpgradeFX`
- Purpose: Applies upgrade-related visual effects.
- Calls: None visible.

### `UpgradeMux::attemptUpgrade`
- Purpose: Attempts to apply an upgrade if conditions are met.
- Calls: `upgradeImplementation`, `performUpgradeFX`, `giveSelfUpgrade`.

### `UpgradeMux::testUpgradeConditions`
- Purpose: Checks if upgrade conditions are satisfied.
- Calls: `getUpgradeActivationMasks`.

## Globals
- None.

## Dependencies
- `Common/Module.h`, `Common/STLTypedefs.h`, `Common/Upgrade.h`
- `GameClient/Drawable.h`, `GameClient/FXList.h`
- `GameLogic/Module/BehaviorModule.h`
- `INI` namespace for parsing utilities.
