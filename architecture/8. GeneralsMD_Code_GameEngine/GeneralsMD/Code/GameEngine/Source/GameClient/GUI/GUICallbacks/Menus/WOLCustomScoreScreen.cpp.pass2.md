# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLCustomScoreScreen.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the Westwood Online (WOL) custom match score screen, serving as a bridge between the game's UI system and the WOL networking layer. It handles screen lifecycle, input routing, and system message processing for the post-match score display in custom games.

## Cross-References
### Incoming
- Called by the WOL menu system when transitioning to/from the score screen
- Invoked by the window manager for input and system message routing
- Referenced in WOL menu flow control (lobby navigation)

### Outgoing
- Interacts with `TheWindowManager` for window focus and message dispatch
- Uses `TheShell` for shutdown notification
- References WOL state management (commented-out code suggests direct WOL API calls)

## Design Patterns
- **Callback-based architecture**: Functions serve as event handlers for UI events
- **Resource management via global pointers**: UI elements cached for efficient access
- **State machine stub**: Empty update function hints at intended WOL state integration

Rules followed. Output under 400 tokens.
