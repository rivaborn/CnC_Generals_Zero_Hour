# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ExperienceScalarUpgrade.h

## Purpose
Defines an upgrade module that modifies an object's experience gain by a scalar value.

## Responsibilities
- Declares `ExperienceScalarUpgradeModuleData` to store the experience scalar value.
- Declares `ExperienceScalarUpgrade` class to apply the upgrade to a `Thing`.
- Provides module macros for memory management and serialization.

## Key Types
- **ExperienceScalarUpgradeModuleData (Class)**: Stores the experience scalar value (`m_addXPScalar`).
- **ExperienceScalarUpgrade (Class)**: Applies the experience scalar upgrade to a `Thing`.
- **ExperienceScalarUpgradeMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **ExperienceScalarUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### `ExperienceScalarUpgradeModuleData::buildFieldParse`
- Purpose: Parses module data from a `MultiIniFieldParse` object.
- Calls: Not inferable (external parsing logic).

### `ExperienceScalarUpgrade::upgradeImplementation`
- Purpose: Applies the experience scalar upgrade to the target `Thing`.
- Calls: Not inferable (implementation in `.cpp` file).

### `ExperienceScalarUpgrade::isSubObjectsUpgrade`
- Purpose: Indicates whether the upgrade applies to sub-objects (returns `false`).
- Calls: None.

## Globals
- None.

## Dependencies
- `UpgradeModule.h` (base class for upgrade modules).
- `Thing` (forward-declared, target of the upgrade).
- `MultiIniFieldParse` (for parsing module data).
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`).
