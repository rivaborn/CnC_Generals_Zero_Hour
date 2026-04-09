# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ExtendedMessageBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the game's modal dialog system, bridging the UI layer with game logic through callbacks. It handles dynamic message box creation, button management, and user input routing, serving as the primary interface for in-game notifications and player prompts.

## Cross-References
### Incoming
- UI systems (e.g., `GameWindowManager`) call `ExMessageBox*` functions for modal dialogs
- Game logic modules invoke callbacks registered with message boxes
- Window system uses `ExtendedMessageBoxSystem` for message handling

### Outgoing
- Calls `TheWindowManager` for window lifecycle management
- Uses `TheNameKeyGenerator` for UI element identification
- Invokes `GadgetStaticTextSetText` for text rendering
- Executes user-provided callbacks on button presses

## Design Patterns
- **Strategy Pattern**: Button callbacks are encapsulated in `WindowExMessageBoxData`, allowing dynamic behavior assignment
- **Factory Method**: `ExMessageBox*` functions act as factory methods for different dialog configurations
- **Observer Pattern**: Message box registers as observer for window events via `ExtendedMessageBoxSystem`
