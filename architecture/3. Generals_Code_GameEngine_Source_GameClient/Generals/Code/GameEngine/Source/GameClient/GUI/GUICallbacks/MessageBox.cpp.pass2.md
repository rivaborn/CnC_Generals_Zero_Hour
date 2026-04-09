# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/MessageBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the core UI dialog system for user confirmation prompts, serving as the primary interface between game logic and the window management system for modal message boxes.

## Cross-References
### Incoming
- ExtendedMessageBox.cpp (uses MessageBox functions as base implementations)
- GameWindowManager.cpp (registers MessageBoxSystem/QuitMessageBoxSystem callbacks)
- Various game systems (e.g., save/load, quit confirmation) that need user input

### Outgoing
- GameWindowManager (for window creation/destruction)
- NameKeyGenerator (for button ID resolution)
- Shell (for input focus management)

## Design Patterns
- **Callback Pattern**: Uses function pointers to handle button clicks, enabling flexible behavior without subclassing
- **Factory Pattern**: Convenience functions (MessageBoxYesNo, etc.) act as factories for different message box configurations
- **Observer Pattern**: Window message handlers act as observers for UI events

Rules followed. Output under 400 tokens.
