# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PowerPlantUpdate.h

## Purpose
Defines the PowerPlantUpdate module for managing power plant rod extension logic in the game.

## Responsibilities
- Manages power plant rod extension timing and state
- Provides interface for controlling rod extension
- Handles periodic updates for power plant mechanics
- Parses configuration data for rod extension parameters

## Key Types
- **PowerPlantUpdateModuleData (Class)**: Holds configuration data for rod extension timing.
- **PowerPlantUpdateInterface (Class)**: Abstract interface for rod extension control.
- **PowerPlantUpdate (Class)**: Main module class implementing power plant update logic.
- **PowerPlantUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **PowerPlantUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### `PowerPlantUpdateModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for module data.
- Calls: `UpdateModuleData::buildFieldParse`

### `PowerPlantUpdate::extendRods`
- Purpose: Controls whether power plant rods should be extended.
- Calls: None visible.

### `PowerPlantUpdate::update`
- Purpose: Handles periodic power plant update logic.
- Calls: None visible.

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `INI` namespace (for parsing utilities)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro system (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
