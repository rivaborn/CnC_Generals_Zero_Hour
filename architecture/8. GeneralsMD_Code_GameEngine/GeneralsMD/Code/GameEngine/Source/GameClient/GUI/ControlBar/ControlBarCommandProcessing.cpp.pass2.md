# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommandProcessing.cpp - Enhanced Analysis

## Architectural Role
This file bridges the UI layer and game logic by translating control bar button clicks into game commands. It enforces command preconditions (e.g., resource checks) and dispatches messages to the game state machine.

## Cross-References
### Incoming
- Called by UI event handlers (e.g., `GameWindowManager`) when control bar buttons are clicked
- Used by `ControlBar` state management (e.g., context switching)

### Outgoing
- Dispatches messages via `TheMessageStream` to `GameLogic`
- Queries `ThePlayerList`, `TheScienceStore`, and `TheInGameUI` for state validation
- Invokes `TheEva` for voice responses and `TheBuildAssistant` for build validation

## Design Patterns
- **Command Pattern**: Encapsulates UI actions as game messages (e.g., `MSG_SELL`, `MSG_DO_SPECIAL_POWER`)
- **State Pattern**: Manages `ControlBar` contexts (e.g., `CB_CONTEXT_MULTI_SELECT`) to gate commands
- **Visitor Pattern**: `selectObjectOfType` iterates objects via a callback (implicit in `forEachObjectOfType`)

*Not inferable*: No clear use of Observer or Factory patterns in this file.
