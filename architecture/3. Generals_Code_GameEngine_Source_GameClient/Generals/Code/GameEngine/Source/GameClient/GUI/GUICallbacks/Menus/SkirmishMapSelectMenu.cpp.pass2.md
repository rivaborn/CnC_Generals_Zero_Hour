# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishMapSelectMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the skirmish map selection menu, acting as a bridge between the UI layer and game state management. It handles user interactions, map data retrieval, and coordination with other menu systems.

## Cross-References
### Incoming
- Called by the window manager when processing UI events for the skirmish map selection menu
- Used by the skirmish game setup flow to manage map selection

### Outgoing
- Calls into `TheMapCache` for map metadata and preview images
- Uses `TheSkirmishGameInfo` to store selected map data
- Interacts with `TheWindowManager` for window hierarchy management
- Depends on `GadgetListBox` and other UI control classes for rendering and input handling

## Design Patterns
- **Observer Pattern**: The menu responds to UI events (GBM_SELECTED, GBM_MOUSE_MOVE) by processing callbacks
- **Mediator Pattern**: Coordinates between multiple UI elements (listbox, radio buttons, preview window) without them referencing each other directly
- **State Management**: Maintains global state (selected map, start positions) that persists across menu interactions
