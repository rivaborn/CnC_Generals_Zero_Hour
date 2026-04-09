# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptConditions.h

## Purpose
Header for the scripting engine's condition evaluation system in Command & Conquer Generals Zero Hour.

## Responsibilities
- Defines the `ScriptConditionsInterface` and its implementation `ScriptConditions`
- Declares condition evaluation methods for game logic checks
- Manages script condition evaluation for AI and mission scripting

## Key Types
- **ScriptConditionsInterface (Class)**: Pure virtual interface for script condition evaluation
- **ScriptConditions (Class)**: Concrete implementation of the script condition evaluator
- **Condition (Class)**: Represents a script condition (forward declaration)
- **ObjectTypes (Class)**: Represents object types (forward declaration)
- **Parameter (Class)**: Represents script parameters (forward declaration)
- **Player (Class)**: Represents game players (forward declaration)

## Key Functions
### `evaluateCondition`
- Purpose: Evaluates a script condition
- Calls: Various `evaluate*` methods based on condition type

### `evaluateAllDestroyed`
- Purpose: Checks if all units of a player are destroyed
- Calls: `playerFromParam`

### `evaluateTeamEnteredAreaEntirely`
- Purpose: Checks if an entire team entered a trigger area
- Calls: `objectTypesFromParam`

### `evaluateSkirmishCommandButtonIsReady`
- Purpose: Checks if a skirmish command button is ready
- Calls: None visible in header

## Globals
- **TheScriptConditions (ScriptConditionsInterface*)**: Singleton instance of the script conditions system

## Dependencies
- `SubsystemInterface` (inherited by `ScriptConditionsInterface`)
- Forward declarations: `Condition`, `ObjectTypes`, `Parameter`, `Player`
- Boolean type `Bool`
