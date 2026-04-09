# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanMapSelectMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the LAN map selection menu, acting as a bridge between the GUI system and the game's networking layer. It handles map list population, preview rendering, and start position management, coordinating with the underlying LAN game options UI.

## Cross-References
### Incoming
- Called by the window manager when the map selection menu is initialized or receives input/system messages
- Used by the LAN game options menu to manage map selection flow

### Outgoing
- Interacts with `TheMapCache` for map metadata and previews
- Communicates with `TheLAN->GetMyGame()` to set map properties and start positions
- Uses `TheWindowManager` and `TheNameKeyGenerator` for UI element management
- Depends on `GadgetListBox` and `GadgetRadioButton` for list and radio button functionality

## Design Patterns
- **Observer Pattern**: The menu responds to system messages (e.g., `GBM_SELECTED`) to handle user interactions.
- **Mediator Pattern**: Coordinates between UI elements (listbox, preview window, buttons) and game logic (map selection, start positions).
- **State Management**: Uses global variables to track UI state (selected map, preview window) across callbacks.
