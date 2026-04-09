# GeneralsMD/Code/GameEngine/Include/GameClient/GUICallbacks.h - Enhanced Analysis

## Architectural Role
This header serves as the central registry for all UI-related callbacks in the SAGE engine, bridging the game's windowing system with its menu hierarchy. It defines the lifecycle and message-handling interfaces for every UI screen, from main menus to in-game overlays, enabling modular UI construction.

## Cross-References
### Incoming
- `GameClient/GameWindow.cpp` (primary consumer, implements these callbacks)
- `GameClient/UI/MenuSystem.cpp` (menu transition logic)
- `GameClient/Network/Lobby.cpp` (LAN/WOL menu handlers)
- `GameClient/Replay/ReplayControls.cpp` (replay UI integration)

### Outgoing
- **Game Logic**: Calls into `GameClient/GameClient.cpp` for game state transitions
- **Networking**: References `Network/NetworkClient.h` for multiplayer UI
- **Audio**: Implicitly tied to `Audio/AudioSystem.h` for menu SFX (via `GameWindow`)

## Design Patterns
- **Callback Registry**: Extern declarations form a global callback table, enabling dynamic UI composition
- **State Machine**: Menu lifecycle functions (`Init/Update/Shutdown`) follow classic state machine patterns
- **Observer**: `ControlBarObserverSystem` suggests an observer pattern for HUD updates (not inferable in header alone)
