# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLMapSelectMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI controller for the Westwood Online map selection menu, bridging the GameSpy overlay system with the game's window management and map caching infrastructure. It handles user interactions for map selection and start position configuration during multiplayer game setup.

## Cross-References
### Incoming
- GameSpy overlay system calls `WOLMapSelectMenuInit` to display the map selection UI
- Window manager dispatches system messages to `WOLMapSelectMenuSystem`
- Input system routes keyboard events to `WOLMapSelectMenuInput`

### Outgoing
- Calls into `TheMapCache` for map metadata and preview images
- Interacts with `TheGameSpyGame` to set map selection and game parameters
- Uses `TheWindowManager` for window creation/destruction and focus management
- Invokes `WOLDisplaySlotList` and `WOLDisplayGameOptions` to update related UI elements

## Design Patterns
- **Observer Pattern**: The menu responds to system messages (GBM_SELECTED, GLM_SELECTED) to handle UI events
- **Mediator Pattern**: Coordinates between multiple subsystems (GameSpy, MapCache, WindowManager) without them referencing each other directly
- **State Pattern**: Different UI states (system maps vs user maps) are managed through radio button selections that trigger different population logic
