# GeneralsMD/Code/GameEngine/Include/GameClient/ExtendedMessageBox.h - Enhanced Analysis

## Architectural Role
This header defines the extended message box system for the game client UI layer, providing a flexible callback-based mechanism for modal dialogs. It bridges the core UI system (GameWindowManager) with game logic that requires user confirmation or notification.

## Cross-References
### Incoming
- Likely called by game logic modules (e.g., mission failure/success handlers, network error dialogs) and UI-related systems (e.g., main menu or in-game pause menu).

### Outgoing
- Depends on `GameWindowManager.h` for base `GameWindow` class and UI rendering infrastructure.

## Design Patterns
- **Callback Pattern**: Uses function pointers (`MessageBoxFunc`) to decouple message box creation from the handling logic, allowing dynamic behavior assignment.
- **Strategy Pattern**: Different message box configurations (Yes/No, Ok/Cancel) are implemented as separate functions, encapsulating the UI behavior for each case.
- **Data Container**: `WindowExMessageBoxData` acts as a lightweight container for callback state, enabling context-specific handling.
