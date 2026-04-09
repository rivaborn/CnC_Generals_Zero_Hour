# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarUnderConstruction.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for displaying construction progress in the control bar, bridging the game's object system with the UI framework. It handles dynamic updates to the construction status display and manages context transitions when construction completes.

## Cross-References
### Incoming
- Called by the control bar's context management system when entering/exiting construction states
- Invoked by the game's object update loop when construction progress changes

### Outgoing
- Uses `GameWindowManager` for UI element lookup
- Interacts with `GameText` for localized strings
- Calls `Drawable` methods to access object state
- Uses `ControlBar` base class methods for common UI operations

## Design Patterns
- **Observer Pattern**: Monitors object construction progress changes to trigger UI updates
- **Context Object Pattern**: Manages different UI states (construction vs. completed) for the control bar
- **Dependency Injection**: Receives `Object` instances to display, decoupling UI from game logic
