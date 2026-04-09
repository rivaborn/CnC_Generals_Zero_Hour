# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/MessageBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the core message box UI component in the SAGE engine's window management system. It provides a thin wrapper around the window manager's `gogoMessageBox` function, handling button callbacks and lifecycle management for modal dialogs.

## Cross-References
### Incoming
- ExtendedMessageBox.cpp (uses similar patterns for extended message boxes)
- Various game modules that need to display modal dialogs (e.g., main menu, game over screens)

### Outgoing
- GameWindowManager (via `TheWindowManager->gogoMessageBox` and `winDestroy`)
- NameKeyGenerator (for button ID lookups)
- Callback functions provided by callers

## Design Patterns
- **Callback Pattern**: Uses function pointers to handle button clicks, allowing flexible behavior without subclassing.
- **Facade Pattern**: Simplifies the complex window management system by providing convenient wrapper functions.
- **Singleton Access**: Relies on global singletons (`TheWindowManager`, `TheNameKeyGenerator`) for service location.

Rules followed. Output under 400 tokens.
