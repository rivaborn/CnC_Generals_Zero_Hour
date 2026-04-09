# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ReplayMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the replay menu UI subsystem, bridging the GUI layer with the replay recording/playback infrastructure. It handles user interactions for replay management while delegating file operations and playback to `TheRecorder`.

## Cross-References
### Incoming
- Called by `TheShell` (window manager) for menu navigation
- Triggered by `GadgetListBox` events for file selection
- Used by `MessageBox` callbacks for confirmation dialogs

### Outgoing
- Calls `TheRecorder` for replay file operations and playback
- Uses `TheFileSystem` for file enumeration
- Interacts with `TheMapCache` for replay metadata
- Leverages `TheShell` for window management

## Design Patterns
- **Command Pattern**: Uses callback functions (`deleteReplayFlag`, `copyReplayFlag`) to decouple UI events from actions
- **Singleton Access**: Relies on global singletons (`TheRecorder`, `TheFileSystem`) for subsystem access
- **Observer Pattern**: Listens for UI events via `ReplayMenuSystem` callback

*Not inferable*: No clear use of Factory, Strategy, or State patterns in this file.
