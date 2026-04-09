# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarCallback.cpp - Enhanced Analysis

## Architectural Role
This file implements the core input handling and state management for the in-game control bar and HUD. It bridges the UI layer with game logic, handling user input routing, control bar visibility animations, and context-sensitive command processing.

## Cross-References
### Incoming
- `GameClient/ControlBar.h` (uses `TheControlBar` singleton)
- `GameClient/InGameUI.h` (queries command state via `TheInGameUI`)
- `GameClient/GameWindowManager.h` (window management via `TheWindowManager`)
- `GameLogic/GameLogic.h` (game state checks)

### Outgoing
- **Input Routing**: Dispatches to `TheRadar`, `TheMouse`, `TheTacticalView`
- **UI State**: Modifies `TheControlBar` stages and animations
- **Game Commands**: Executes via `TheGameClient->evaluateContextCommand()`
- **Messaging**: Uses `TheMessageStream` for feedback

## Design Patterns
- **Singleton Access**: Relies on global singletons (`TheControlBar`, `TheRadar`, etc.) for cross-subsystem communication
- **Event-Driven Handling**: Processes window messages in a switch-based dispatch pattern
- **State Machine**: Control bar visibility toggling uses implicit state transitions (e.g., `CONTROL_BAR_STAGE_DEFAULT`)

*Not inferable*: No clear use of Observer or Strategy patterns despite context-sensitive behavior.
