# GeneralsMD/Code/GameEngine/Source/GameLogic/System/GameLogicDispatch.cpp - Enhanced Analysis

## Architectural Role
Central message router for game logic, bridging player input, AI commands, and game state transitions. Acts as the primary dispatcher for all game messages, coordinating between subsystems like AI, UI, and networking.

## Cross-References
### Incoming
- `GameClient/CommandXlat.h` (translates input commands)
- `GameNetwork/NetworkInterface.h` (handles network messages)
- `GameLogic/AI.h` (AI group management)
- `GameClient/InGameUI.h` (UI feedback)

### Outgoing
- Calls into `Player` for team/selection commands
- Invokes `AIUpdateInterface` for movement/rally logic
- Uses `Recorder` for replay handling
- Interfaces with `GameAudio` for sound cues

## Design Patterns
- **Command Pattern**: Encapsulates game actions (e.g., `doMoveTo`) as message handlers
- **Observer Pattern**: Notifies subsystems (UI, audio) of state changes via global singletons
- **State Pattern**: Manages game state transitions (e.g., `prepareNewGame`, `clearGameData`)

*Not inferable*: Exact pattern usage in truncated sections (e.g., CRC validation flow).
