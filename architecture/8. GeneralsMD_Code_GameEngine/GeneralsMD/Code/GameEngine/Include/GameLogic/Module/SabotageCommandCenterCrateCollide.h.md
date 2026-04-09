# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageCommandCenterCrateCollide.h

## Purpose
Defines a crate collision module that resets all Command Center general powers when triggered.

## Responsibilities
- Inherits from `CrateCollide` to handle crate collision behavior
- Validates if the collision should execute
- Executes the sabotage behavior (resetting powers)
- Identifies itself as a sabotage building crate

## Key Types
- **SabotageCommandCenterCrateCollideModuleData (Class)**: Module data container with field parsing
- **SabotageCommandCenterCrateCollide (Class)**: Main crate collision handler
- **SabotageCommandCenterCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object

## Key Functions
### `isValidToExecute`
- Purpose: Determines if the collision should execute
- Calls: Not inferable

### `executeCrateBehavior`
- Purpose: Executes the sabotage behavior (resetting powers)
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/Module.h`
- `GameLogic/Module/CrateCollide.h`
- `MultiIniFieldParse` (used in `buildFieldParse`)
- `Object` (forward reference)
- `Bool` (likely from engine typedefs)
