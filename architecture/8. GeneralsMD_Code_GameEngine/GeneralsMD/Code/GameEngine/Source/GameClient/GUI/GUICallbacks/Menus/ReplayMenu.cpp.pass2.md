# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ReplayMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the replay browser UI, bridging the GUI system with the replay recording/playback infrastructure. It handles file operations, metadata display, and user interactions for replay management.

## Cross-References
### Incoming
- Called by `TheShell` (window manager) when replay menu is activated
- Used by `GameWindowTransitions` for menu animations
- Referenced by `GameWindowManager` for window lifecycle

### Outgoing
- Calls `TheRecorder` for replay file operations and metadata
- Uses `GadgetListBox` functions for UI list management
- Invokes `MessageBox` for user confirmation dialogs
- Accesses `TheMapCache` for map metadata display

## Design Patterns
- **Callback Pattern**: Uses event-driven callbacks for UI interactions (e.g., button clicks)
- **Singleton Access**: Relies on global singletons (`TheRecorder`, `TheGameText`) for shared services
- **State Management**: Uses global flags (`callCopy`, `callDelete`) for deferred operations

*Not inferable*: No clear use of Observer or Factory patterns in this file.
