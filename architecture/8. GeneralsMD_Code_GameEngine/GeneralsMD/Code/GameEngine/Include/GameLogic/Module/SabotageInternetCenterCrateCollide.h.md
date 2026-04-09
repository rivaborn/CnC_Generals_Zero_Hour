# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageInternetCenterCrateCollide.h

## Purpose
Defines a crate collision module that temporarily disables an internet center when triggered.

## Responsibilities
- Handles collision logic for sabotage crates
- Manages sabotage duration timing
- Validates target objects for sabotage
- Executes sabotage behavior on valid targets
- Provides module data parsing for configuration

## Key Types
- **SabotageInternetCenterCrateCollideModuleData (Class)**: Stores sabotage duration configuration
- **SabotageInternetCenterCrateCollide (Class)**: Implements sabotage crate collision behavior
- **SabotageInternetCenterCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object type

## Key Functions
### SabotageInternetCenterCrateCollideModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: CrateCollideModuleData::buildFieldParse

### SabotageInternetCenterCrateCollide::isValidToExecute
- Purpose: Determines if sabotage can be applied to target object
- Calls: Not inferable

### SabotageInternetCenterCrateCollide::executeCrateBehavior
- Purpose: Applies sabotage effect to valid target
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- MultiIniFieldParse, INI namespace (for parsing)
- Memory pool and module macro systems (internal)
