# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanMapSelectMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the LAN map selection menu, acting as a bridge between the UI layer and the game's networking/map systems. It handles user interactions (map selection, start positions) and updates the game state accordingly.

## Cross-References
### Incoming
- Called by the window manager when handling system messages for the map selection menu
- Invoked by the LAN game options menu when transitioning to map selection

### Outgoing
- Calls into `TheMapCache` for map metadata and preview images
- Interacts with `TheLAN->GetMyGame()` to set map and start position data
- Uses `TheWindowManager` for UI element management
- Calls `PostToLanGameOptions` to communicate back to the parent menu

## Design Patterns
- **Observer Pattern**: The menu responds to system messages (GBM_SELECTED, GLM_SELECTED) to handle UI events
- **Mediator Pattern**: Coordinates between multiple UI elements (listbox, preview, buttons) and game systems
- **State Management**: Maintains global state for UI elements and map selection data

Rules followed. Output under 400 tokens.
