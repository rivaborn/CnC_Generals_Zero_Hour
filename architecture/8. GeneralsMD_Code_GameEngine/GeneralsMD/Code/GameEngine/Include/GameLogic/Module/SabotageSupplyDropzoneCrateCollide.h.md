# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageSupplyDropzoneCrateCollide.h

## Purpose
Defines a crate collision module that simulates a saboteur stealing cash from power plants when colliding.

## Responsibilities
- Handles collision logic for sabotage crates
- Manages cash theft mechanics
- Validates collision targets
- Provides module data parsing

## Key Types
- **SabotageSupplyDropzoneCrateCollideModuleData (Class)**: Stores configuration data including cash theft amount
- **SabotageSupplyDropzoneCrateCollide (Class)**: Implements the sabotage crate collision behavior
- **SabotageSupplyDropzoneCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object

## Key Functions
### SabotageSupplyDropzoneCrateCollideModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: CrateCollideModuleData::buildFieldParse

### SabotageSupplyDropzoneCrateCollide::isValidToExecute
- Purpose: Determines if collision target is valid for sabotage
- Calls: Not inferable

### SabotageSupplyDropzoneCrateCollide::executeCrateBehavior
- Purpose: Executes the cash theft behavior on valid targets
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- INI parsing utilities
- Memory pool macros
- Module data framework
