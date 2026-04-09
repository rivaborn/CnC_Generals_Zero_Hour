# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/LifetimeUpdate.h

## Purpose
Defines a game module that manages object lifetime by counting down frames and destroying the object when the count reaches zero.

## Responsibilities
- Manages object lifetime via frame counting
- Provides configuration for min/max lifetime frames
- Handles object destruction when lifetime expires
- Supports module data parsing from INI files

## Key Types
- **LifetimeUpdateModuleData (Class)**: Holds min/max lifetime frame values and INI parsing logic
- **LifetimeUpdate (Class)**: Implements the update module that counts down frames
- **LifetimeUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **LifetimeUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### LifetimeUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsers for min/max lifetime values
- Calls: UpdateModuleData::buildFieldParse

### LifetimeUpdate::update
- Purpose: Updates the frame counter and returns sleep time
- Calls: calcSleepDelay

### LifetimeUpdate::calcSleepDelay
- Purpose: Calculates sleep delay based on min/max frame range
- Calls: None

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for INI parsing)
- INI namespace (for parseDurationUnsignedInt)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
