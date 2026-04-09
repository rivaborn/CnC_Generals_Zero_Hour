# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ActiveShroudUpgrade.h

## Purpose
Defines an upgrade module that modifies an object's shroud range in the game.

## Responsibilities
- Declares `ActiveShroudUpgradeModuleData` to store upgrade configuration.
- Declares `ActiveShroudUpgrade` class to apply shroud range upgrades.
- Provides memory management macros for object pooling.
- Defines module creation and serialization macros.

## Key Types
- **ActiveShroudUpgradeModuleData (Class)**: Stores the new shroud range value for the upgrade.
- **ActiveShroudUpgrade (Class)**: Applies the shroud range upgrade to a game object.
- **ActiveShroudUpgradeMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **ActiveShroudUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### ActiveShroudUpgradeModuleData::buildFieldParse
- Purpose: Parses configuration data for the upgrade module.
- Calls: Not inferable (likely uses `MultiIniFieldParse` methods).

### ActiveShroudUpgrade::upgradeImplementation
- Purpose: Applies the shroud range upgrade to the target object.
- Calls: Not inferable (likely modifies object properties).

### ActiveShroudUpgrade::isSubObjectsUpgrade
- Purpose: Indicates whether the upgrade applies to sub-objects.
- Calls: None.

## Globals
None.

## Dependencies
- `UpgradeModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `Thing`, `Player`, `ObjectCreationList` (forward references)
