# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageSuperweaponCrateCollide.h

## Purpose
Defines a crate collision module for sabotaging superweapons in Command & Conquer Generals Zero Hour.

## Responsibilities
- Handles collision logic for sabotage superweapon crates
- Validates collision targets
- Executes sabotage behavior on valid targets
- Provides module data parsing for configuration

## Key Types
- **SabotageSuperweaponCrateCollideModuleData (Class)**: Module data container with field parsing
- **SabotageSuperweaponCrateCollide (Class)**: Main crate collision handler for sabotage behavior
- **SabotageSuperweaponCrateCollideMagicEnum (Enum)**: Not inferable (empty enum)
- **SabotageSuperweaponCrateCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### SabotageSuperweaponCrateCollideModuleData::buildFieldParse
- Purpose: Configures field parsing for module data
- Calls: CrateCollideModuleData::buildFieldParse

### SabotageSuperweaponCrateCollide::isValidToExecute
- Purpose: Determines if collision target is valid for sabotage
- Calls: None visible

### SabotageSuperweaponCrateCollide::executeCrateBehavior
- Purpose: Executes sabotage behavior on valid targets
- Calls: None visible

### SabotageSuperweaponCrateCollide::isSabotageBuildingCrateCollide
- Purpose: Identifies this as a sabotage building crate collision
- Calls: None visible

## Globals
- None

## Dependencies
- Common/Module.h
- GameLogic/Module/CrateCollide.h
- Thing (forward reference)
- MultiIniFieldParse (used in buildFieldParse)
- Object (used
