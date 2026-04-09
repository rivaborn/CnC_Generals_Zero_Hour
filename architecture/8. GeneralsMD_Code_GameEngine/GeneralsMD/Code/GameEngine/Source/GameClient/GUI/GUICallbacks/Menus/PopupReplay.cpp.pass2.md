# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupReplay.cpp - Enhanced Analysis

## Architectural Role
This file implements the replay save/load UI subsystem, bridging the UI layer with the game's replay recording system. It handles user interactions for replay management while coordinating with the recorder and filesystem subsystems.

## Cross-References
### Incoming
- **GameClient/GUI/GUICallbacks.h**: Registers `PopupReplaySystem` as a window message handler
- **GameClient/Shell.cpp**: Likely invokes `PopupReplayInit` during menu initialization
- **GameLogic/GameLogic.cpp**: May call `ShowReplaySavedPopup` after replay operations

### Outgoing
- **Common/Recorder.h**: Uses `TheRecorder` for replay path/extension and actual recording
- **Common/LocalFileSystem.h**: File existence checks and operations via `TheLocalFileSystem`
- **GameClient/GadgetListBox.h**: Populates and queries the replay file listbox
- **GameClient/MessageBox.h**: Shows confirmation dialogs for overwrite scenarios

## Design Patterns
- **Observer Pattern**: The `PopupReplaySystem` handler observes UI events (button clicks, text changes) and reacts accordingly
- **Mediator Pattern**: Coordinates between UI controls (listbox, text entry, buttons) without direct coupling
- **State Pattern**: Implicitly manages the "replay saved" popup state via `ShowReplaySavedPopup`

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns in the visible code.
