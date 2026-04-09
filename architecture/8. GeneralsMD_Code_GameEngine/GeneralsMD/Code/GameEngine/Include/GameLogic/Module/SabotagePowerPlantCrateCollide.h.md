# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotagePowerPlantCrateCollide.h

## Purpose
Defines a crate collision module that sabotages power plants by disabling their power output for a set duration.

## Responsibilities
- Handles collision logic for sabotage crates targeting power plants
- Manages power plant sabotage duration via module data
- Validates collision targets and executes sabotage behavior
- Provides module data parsing for configuration

## Key Types
- **SabotagePowerPlantCrateCollideModuleData (Class)**: Stores sabotage duration configuration
- **SabotagePowerPlantCrateCollide (Class)**: Implements power plant sabotage crate collision behavior
- **SabotagePowerPlantCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object type

## Key Functions
### SabotagePowerPlantCrateCollideModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: CrateCollideModuleData::buildFieldParse

### SabotagePowerPlantCrateCollide::isValidToExecute
- Purpose: Determines if the collision target is valid for sabotage
- Calls: None visible

### SabotagePowerPlantCrateCollide::executeCrateBehavior
- Purpose: Executes the power plant sabotage logic
- Calls: None visible

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- MultiIniFieldParse, INI namespace (for field parsing)
- Memory pool and module macro systems (internal SAGE framework)
