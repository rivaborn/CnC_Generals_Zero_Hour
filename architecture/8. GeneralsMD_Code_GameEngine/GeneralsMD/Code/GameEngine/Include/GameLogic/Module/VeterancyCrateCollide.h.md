# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/VeterancyCrateCollide.h

## Purpose
Defines a crate module that grants veterancy experience to nearby units when collided with.

## Responsibilities
- Handles veterancy crate collision logic
- Manages veterancy experience distribution
- Validates collision targets
- Configures veterancy crate behavior via module data

## Key Types
- **VeterancyCrateCollideModuleData (Class)**: Stores veterancy crate configuration (range, owner veterancy flag, pilot flag)
- **VeterancyCrateCollide (Class)**: Implements veterancy crate collision behavior
- **VeterancyCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object

## Key Functions
### VeterancyCrateCollideModuleData::buildFieldParse
- Purpose: Registers INI field parsing for veterancy crate module data
- Calls: CrateCollideModuleData::buildFieldParse

### VeterancyCrateCollide::isValidToExecute
- Purpose: Determines if a collision target is valid for veterancy crate
- Calls: None visible

### VeterancyCrateCollide::executeCrateBehavior
- Purpose: Applies veterancy experience to valid collision targets
- Calls: None visible

### VeterancyCrateCollide::getLevelsToGain
- Purpose: Calculates veterancy levels to grant
- Calls: None visible

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- INI parsing utilities
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro system (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
