# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpyVisionSpecialPower.h

## Purpose
Defines the spy vision special power module for the game, allowing a player to spy on enemy vision.

## Responsibilities
- Declares the `SpyVisionSpecialPowerModuleData` class for configuration.
- Declares the `SpyVisionSpecialPower` class implementing the special power logic.
- Provides memory management macros for the special power class.
- Defines enums for magic values and module creation.

## Key Types
- **SpyVisionSpecialPowerModuleData (Class)**: Holds configuration data for spy vision duration.
- **SpyVisionSpecialPower (Class)**: Implements the spy vision special power functionality.
- **SpyVisionSpecialPowerMagicEnum (Enum)**: Not inferable (empty).
- **SpyVisionSpecialPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty).

## Key Functions
### `SpyVisionSpecialPowerModuleData::buildFieldParse`
- Purpose: Parses configuration fields for the module data.
- Calls: Not inferable.

### `SpyVisionSpecialPower::doSpecialPower`
- Purpose: Executes the spy vision special power logic.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `SpecialPowerModule.h` (included)
- `MultiIniFieldParse` (used in `buildFieldParse`)
- `Thing` (used in constructor)
- `ModuleData` (used in constructor)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
