# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptEngine.h - Enhanced Analysis

## Architectural Role
This header defines the central scripting system that bridges game logic, AI behavior, and mission scripting. It acts as the runtime interpreter for the game's script language, coordinating between game state evaluation and action execution.

## Cross-References
### Incoming
- AI subsystem (uses `evaluateConditions` for decision making)
- Mission system (calls `runScript` for scripted events)
- Game loop (invokes `update` for frame-by-frame script processing)

### Outgoing
- Object/Thing system (accesses `Object` and `ThingTemplate` instances)
- Team/Player management (references `Team` and `Player` classes)
- Snapshot system (implements serialization for save/load)

## Design Patterns
- **Singleton Pattern**: `TheScriptEngine` provides global access to the scripting system
- **Command Pattern**: Script actions/conditions encapsulate operations as objects
- **Observer Pattern**: Scripts react to game state changes via condition evaluation

*Not inferable*: Exact implementation of script parsing/execution flow.
