# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MoneyCrateCollide.h

## Purpose
Defines a game module for money crates that provide funds when collided with.

## Responsibilities
- Manages money crate collision behavior
- Handles money distribution to colliding objects
- Supports upgrade-based supply boosts
- Parses configuration data from INI files

## Key Types
- **MoneyCrateCollideModuleData (Class)**: Stores money amount and upgrade boosts
- **MoneyCrateCollide (Class)**: Implements money crate collision logic
- **MoneyCrateCollideMagicEnum (Enum)**: Not inferable
- **MoneyCrateCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### MoneyCrateCollideModuleData::buildFieldParse
- Purpose: Parses INI configuration for money crate properties
- Calls: CrateCollideModuleData::buildFieldParse

### MoneyCrateCollide::executeCrateBehavior
- Purpose: Handles money distribution when crate is collided with
- Calls: Not inferable

### MoneyCrateCollide::getUpgradedSupplyBoost
- Purpose: Calculates supply boost based on object upgrades
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- GameLogic/Module/AutoDepositUpdate.h
- Thing class (forward reference)
- INI parsing utilities (parseUpgradePair)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macros (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
