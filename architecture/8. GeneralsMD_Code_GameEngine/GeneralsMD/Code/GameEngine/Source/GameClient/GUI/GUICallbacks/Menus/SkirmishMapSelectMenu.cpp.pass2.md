# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishMapSelectMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI controller for the skirmish map selection menu, bridging the UI layer with game data systems. It handles user interactions, map list population, and preview rendering, acting as a mediator between the UI framework and core game systems like `TheMapCache` and `TheSkirmishGameInfo`.

## Cross-References
### Incoming
- Called by UI event system when map selection menu is active
- Invoked by parent menu system when transitioning to map selection

### Outgoing
- Calls `TheMapCache` for map metadata and preview images
- Updates `TheSkirmishGameInfo` with selected map data
- Interacts with `TheWindowManager` for UI element management
- Uses `TheNameKeyGenerator` for window ID lookups

## Design Patterns
- **Mediator Pattern**: Coordinates between UI elements and game data systems without tight coupling
- **Observer Pattern**: Reacts to UI events (selections, button clicks) to update game state
- **Singleton Access**: Uses global singletons (`TheMapCache`, `TheSkirmishGameInfo`) for shared state
