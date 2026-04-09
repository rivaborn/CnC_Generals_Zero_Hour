# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/InGamePopupMessage.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI callback system for in-game popup messages, bridging the game's message system with the window management framework. It handles dynamic UI generation, input routing, and modal behavior for notifications.

## Cross-References
### Incoming
- Called by `TheWindowManager` during window initialization and message processing
- Triggered by `TheInGameUI` when popup messages are queued
- Input events routed through `TheWindowManager`'s message system

### Outgoing
- Interacts with `TheWindowManager` for window creation/destruction and focus management
- Uses `TheMessageStream` for game message handling
- Depends on `TheInGameUI` for popup data management
- Leverages `TheDisplayStringManager` for text rendering and measurement

## Design Patterns
- **Callback Pattern**: Uses window message callbacks for event-driven UI behavior
- **Dependency Injection**: Receives `PopupMessageData` from `TheInGameUI` for dynamic content
- **Modal Dialog Pattern**: Implements pause functionality and focus trapping for modal behavior
