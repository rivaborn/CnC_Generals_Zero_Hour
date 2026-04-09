# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CheckpointUpdate.h

## Purpose
Defines a game logic module that triggers updates when enemies or allies are detected within a specified range.

## Responsibilities
- Detects nearby enemies and allies
- Manages scan delay timing
- Provides module data parsing for configuration
- Handles update logic for game objects

## Key Types
- **CheckpointUpdateModuleData (Class)**: Holds module configuration including enemy scan delay time
- **CheckpointUpdate (Class)**: Main module class that implements update logic
- **CheckpointUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CheckpointUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### CheckpointUpdateModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: UpdateModuleData::buildFieldParse

### CheckpointUpdate::update
- Purpose: Main update function that checks for enemies/allies and manages sleep timing
- Calls: checkForAlliesAndEnemies

### CheckpointUpdate::checkForAlliesAndEnemies
- Purpose: Scans for nearby enemies and allies within detection range
- Calls: Not inferable from header

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for configuration parsing)
- INI parsing utilities
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro system (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
