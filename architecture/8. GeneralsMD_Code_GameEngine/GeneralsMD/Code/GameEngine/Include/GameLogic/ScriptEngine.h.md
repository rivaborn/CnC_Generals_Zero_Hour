# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptEngine.h

## Purpose
Header defining the ScriptEngine class, which manages game scripting, conditions, actions, and sequential script execution.

## Responsibilities
- Manages script execution and evaluation
- Handles game state conditions and actions
- Controls sequential script execution
- Maintains game counters, flags, and attack priorities
- Manages map reveals and object tracking

## Key Types
- **ScriptEngine (Class)**: Core scripting engine managing game logic scripts
- **SequentialScript (Class)**: Handles sequential script execution
- **AttackPriorityInfo (Class)**: Manages attack priority settings
- **BreezeInfo (Struct)**: Stores wind/breeze simulation parameters
- **NamedReveal (Struct)**: Defines named map reveal areas

## Key Functions
### `runScript`
- Purpose: Executes a named script for a team
- Calls: `findScript`, `executeScripts`

### `evaluateConditions`
- Purpose: Evaluates script conditions for a team/object
- Calls: `evaluateCondition`, `checkConditionsForTeamNames`

### `executeActions`
- Purpose: Executes script actions
- Calls: Various action-specific handlers like `setCounter`, `setFlag`

### `update`
- Purpose: Updates script engine state each frame
- Calls: `evaluateAndProgressAllSequentialScripts`, `updateFades`

## Globals
- **TheScriptEngine (ScriptEngine*)**: Singleton instance of the script engine

## Dependencies
- Common game types and memory management headers
- Snapshot system for save/load
- STL containers and typedefs
- Script system headers
- Various game object class forward declarations
