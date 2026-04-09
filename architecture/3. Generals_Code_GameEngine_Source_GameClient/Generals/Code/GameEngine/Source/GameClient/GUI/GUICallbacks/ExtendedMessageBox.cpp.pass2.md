# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ExtendedMessageBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer's modal dialog system, bridging the window management subsystem with user interaction callbacks. It extends the base message box functionality by supporting custom button layouts and callback mechanisms, critical for in-game notifications and user prompts.

## Cross-References
### Incoming
- `GameClient/GUI/GUICallbacks/ExtendedMessageBox.h` (header)
- `GameClient/GameWindowManager.h` (window creation/destruction)
- `GameClient/GadgetStaticText.h` (text display)
- Various UI event handlers (button clicks, focus changes)

### Outgoing
- `TheWindowManager` (window lifecycle)
- `TheNameKeyGenerator` (UI element identification)
- Callback functions passed by clients (game logic, menus)

## Design Patterns
- **Strategy Pattern**: Uses callback functions to encapsulate different behaviors for button clicks
- **Factory Method**: Convenience functions (`ExMessageBoxYesNo`, etc.) act as factory methods for different dialog types
- **Observer Pattern**: Window message system acts as observer for UI events

Rules followed. Output under 400 tokens.
