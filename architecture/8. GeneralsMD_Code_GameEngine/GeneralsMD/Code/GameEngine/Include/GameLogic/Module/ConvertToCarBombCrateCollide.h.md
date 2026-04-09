# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ConvertToCarBombCrateCollide.h

## Purpose
Defines a crate module that converts cars into car bombs upon collision, triggering their weapons and AI.

## Responsibilities
- Handles collision logic for car bomb crates
- Manages conversion of cars into car bombs
- Provides module data parsing for game configuration
- Implements crate behavior execution

## Key Types
- **ConvertToCarBombCrateCollideModuleData (Class)**: Stores module configuration (effect range, FX list)
- **ConvertToCarBombCrateCollide (Class)**: Implements the car bomb conversion crate behavior
- **ConvertToCarBombCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object
- **FXList (Class)**: Forward reference to effects list

## Key Functions
### ConvertToCarBombCrateCollideModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: CrateCollideModuleData::buildFieldParse

### ConvertToCarBombCrateCollide::isValidToExecute
- Purpose: Determines if the crate can execute on a given object
- Calls: None visible

### ConvertToCarBombCrateCollide::executeCrateBehavior
- Purpose: Executes the car bomb conversion logic
- Calls: None visible

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- INI parsing utilities (parseFXList)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
