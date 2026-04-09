# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageSupplyCenterCrateCollide.h

## Purpose
Defines a crate module that simulates a saboteur stealing cash from a supply center upon collision.

## Responsibilities
- Inherits from `CrateCollide` to handle supply center sabotage logic
- Manages cash theft amount via module data
- Validates collision targets and executes sabotage behavior
- Provides memory management and module registration macros

## Key Types
- **SabotageSupplyCenterCrateCollideModuleData (Class)**: Stores configuration (cash theft amount)
- **SabotageSupplyCenterCrateCollide (Class)**: Implements sabotage crate behavior
- **Thing (Class)**: Forward reference to game object (not defined here)

## Key Functions
### `isValidToExecute`
- Purpose: Determines if sabotage can be applied to the target object
- Calls: Not inferable

### `executeCrateBehavior`
- Purpose: Executes the cash theft sabotage logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/Module.h` (base module infrastructure)
- `GameLogic/Module/CrateCollide.h` (parent crate collision class)
- `INI` namespace (for field parsing)
- `MultiIniFieldParse` (configuration parsing utility)
