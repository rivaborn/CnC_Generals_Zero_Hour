# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageMilitaryFactoryCrateCollide.h

## Purpose
Defines a crate module that temporarily disables a military factory when collided with.

## Responsibilities
- Handles collision logic for sabotage crates
- Manages factory disable duration
- Validates collision targets
- Executes sabotage behavior

## Key Types
- **SabotageMilitaryFactoryCrateCollideModuleData (Class)**: Stores sabotage duration configuration
- **SabotageMilitaryFactoryCrateCollide (Class)**: Implements sabotage crate collision behavior
- **SabotageMilitaryFactoryCrateCollideMagicEnum (Enum)**: Not inferable
- **SabotageMilitaryFactoryCrateCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### SabotageMilitaryFactoryCrateCollideModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: CrateCollideModuleData::buildFieldParse

### SabotageMilitaryFactoryCrateCollide::isValidToExecute
- Purpose: Determines if collision target is valid for sabotage
- Calls: None

### SabotageMilitaryFactoryCrateCollide::executeCrateBehavior
- Purpose: Applies sabotage effect to target factory
- Calls: None

## Globals
None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- Thing (forward reference)
