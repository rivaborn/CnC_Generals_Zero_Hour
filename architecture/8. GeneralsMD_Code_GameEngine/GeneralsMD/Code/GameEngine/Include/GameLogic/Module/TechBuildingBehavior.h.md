# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TechBuildingBehavior.h

## Purpose
Defines behavior for tech buildings in the game, handling updates, capture events, and destruction.

## Responsibilities
- Manages tech building updates and pulse effects
- Handles building capture transitions
- Implements destruction logic via DieModuleInterface
- Provides module data parsing for configuration

## Key Types
- **TechBuildingBehaviorModuleData (Class)**: Stores pulse FX and rate for building ownership changes
- **TechBuildingBehavior (Class)**: Core behavior module for tech buildings
- **TechBuildingBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **TechBuildingBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### TechBuildingBehaviorModuleData::buildFieldParse
- Purpose: Parses configuration data for the module
- Calls: Not inferable

### TechBuildingBehavior::onCapture
- Purpose: Handles building ownership transfer events
- Calls: Not inferable

### TechBuildingBehavior::update
- Purpose: Updates building state and pulse effects
- Calls: Not inferable

### TechBuildingBehavior::onDie
- Purpose: Executes destruction logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/DieModule.h`
- `GameLogic/Module/UpdateModule.h`
- `MultiIniFieldParse` (external)
- `FXList` (external)
- `Thing`, `Player`, `DamageInfo` (external)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
