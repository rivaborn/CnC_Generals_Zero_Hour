# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DisconnectWindow.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for network disconnection handling, bridging the GUI system with the game's networking layer. It manages the disconnect menu's lifecycle, input handling, and communication with the `DisconnectMenu` subsystem.

## Cross-References
### Incoming
- `DisconnectMenu.h` (calls `quitGame`, `voteForPlayer`, `sendChat`)
- `GameWindowManager.h` (uses `winCreateLayout`, `winGetWindowFromId`)
- `NameKeyGenerator.h` (uses `nameToKey`)

### Outgoing
- `GadgetTextEntry.h` (uses `GadgetTextEntrySetText`, `GadgetTextEntryGetText`)
- `GadgetListBox.h` (uses `GadgetListBoxReset`, `GadgetListBoxAddEntryText`)
- `GameText.h` (uses `fetch` for localized text)

## Design Patterns
- **Singleton Access**: Relies on global singletons (`TheWindowManager`, `TheDisconnectMenu`) for subsystem access.
- **Event-Driven Handling**: Uses message-based callbacks (`GBM_SELECTED`, `GEM_EDIT_DONE`) for UI interactions.
- **Lazy Initialization**: Loads the menu layout only when first shown (`disconnectMenuLayout == NULL` check).
