# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptActions.h - Enhanced Analysis

## Architectural Role
This header defines the core scripting interface for the SAGE engine, bridging the game's logic layer with its scripting system. It serves as the primary mechanism for external scripts to manipulate game state, camera, audio, and UI, making it a critical cross-cutting component.

## Cross-References
### Incoming
- Scripting engine (e.g., `ScriptEngine.cpp`) - calls `executeAction` to dispatch script commands
- Mission/level files - reference script action names (e.g., `doVictory`, `doDefeat`)
- UI systems - use `doDisplayText`/`doMoviePlayFullScreen` for in-game messages/cinematics

### Outgoing
- **Camera subsystem** - calls `doCameraMoveTo`, `doCameraFollowNamed` (likely via `View`/`Camera` classes)
- **Audio system** - uses `doPlaySoundEffect`, `doSpeechPlay` (ties to `AudioAffect` enum)
- **Game state** - modifies teams/units via `doTeamAttackArea`, `doNamedAttack`
- **UI layer** - interacts with `GameWindow` for popups/messages

## Design Patterns
- **Singleton** - `TheScriptActions` provides global access to script execution
- **Command Pattern** - Each `doXxx` method encapsulates a discrete game operation
- **Facade** - Hides complexity of subsystems behind simple scriptable interfaces (e.g., camera control)

*Not inferable*: Exact implementation of `ScriptAction` hierarchy or how scripts are parsed/loaded.
