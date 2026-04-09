# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/EnemyNearUpdate.h

## Purpose
Defines a game logic module that detects when enemies are within a specified range and triggers updates accordingly.

## Responsibilities
- Detects nearby enemies based on a configurable scan delay.
- Provides module data for configuration via INI parsing.
- Inherits from `UpdateModule` for periodic updates.
- Uses memory pooling for object management.

## Key Types
- **EnemyNearUpdateModuleData (Class)**: Holds configuration data (scan delay time) for the module.
- **EnemyNearUpdate (Class)**: Main module class that performs enemy detection and updates.
- **EnemyNearUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **EnemyNearUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### `EnemyNearUpdateModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for module data.
- Calls: `UpdateModuleData::buildFieldParse`, `p.add`

### `EnemyNearUpdate::update`
- Purpose: Periodically checks for nearby enemies and updates state.
- Calls: `checkForEnemies`

### `EnemyNearUpdate::checkForEnemies`
- Purpose: Scans for enemies within range and updates `m_enemyNear` flag.
- Calls: Not inferable (implementation in .cpp).

## Globals
None.

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse` (INI parsing)
- `INI` namespace (parsing utilities)
- `Thing` (game entity base class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
