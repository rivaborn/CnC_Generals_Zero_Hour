# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageFakeBuildingCrateCollide.h

## Purpose
Defines a crate collision module that simulates a saboteur destroying a fake building.

## Responsibilities
- Extends `CrateCollide` to handle sabotage behavior
- Validates collision targets
- Executes sabotage logic on valid targets
- Provides module data parsing

## Key Types
- **SabotageFakeBuildingCrateCollideModuleData (Class)**: Module data for sabotage crate behavior
- **SabotageFakeBuildingCrateCollide (Class)**: Main sabotage crate collision handler
- **SabotageFakeBuildingCrateCollideMagicEnum (Enum)**: Not inferable (empty)
- **SabotageFakeBuildingCrateCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### `isValidToExecute`
- Purpose: Checks if collision target is valid for sabotage
- Calls: None

### `executeCrateBehavior`
- Purpose: Executes sabotage logic on valid targets
- Calls: None

## Globals
- None

## Dependencies
- `Common/Module.h`
- `GameLogic/Module/CrateCollide.h`
- `Thing` (forward reference)
- `MultiIniFieldParse` (external)
- `Object` (external)
- `Bool` (external)
