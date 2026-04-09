# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DisconnectWindow.cpp

## Purpose
Handles the network disconnect menu UI, including player voting and chat functionality.

## Responsibilities
- Manages the disconnect menu window layout and controls
- Handles user input for chat and player voting
- Interfaces with the disconnect menu system for game actions

## Key Types
- `WindowLayout` (Type): UI layout container
- `GameWindow` (Type): UI window element
- `NameKeyType` (Type): Identifier for UI elements

## Key Functions
### `InitDisconnectWindow`
- Purpose: Initializes UI element references from the window layout
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `GadgetTextEntrySetText`, `TheWindowManager->winSetFocus`

### `ShowDisconnectWindow`
- Purpose: Displays the disconnect menu and initializes its state
- Calls: `TheWindowManager->winCreateLayout`, `InitDisconnectWindow`, `disconnectMenuLayout->hide`, `buttonVotePlayerXWindow->winEnable`, `disconnectMenuLayout->bringForward`, `GadgetListBoxReset`, `GadgetListBoxAddEntryText`

### `HideDisconnectWindow`
- Purpose: Hides the disconnect menu
- Calls: `TheWindowManager->winCreateLayout`, `InitDisconnectWindow`, `disconnectMenuLayout->hide`

### `DisconnectControlSystem`
- Purpose: Handles UI event messages for the disconnect menu
- Calls: `TheDisconnectMenu->quitGame`, `TheDisconnectMenu->voteForPlayer`, `GadgetTextEntryGetText`, `GadgetTextEntrySetText`, `TheDisconnectMenu->sendChat`

## Globals
- `disconnectMenuLayout` (WindowLayout*): Stores the loaded menu layout
- `textEntryID`/`textDisplayID` (NameKeyType): IDs for text input/output controls
- `buttonQuitID`/`buttonVotePlayerXID` (NameKeyType): IDs for action buttons
- `textEntryWindow`/`textDisplayWindow` (GameWindow*): References to text controls
- `buttonQuitWindow`/`buttonVotePlayerXWindow` (GameWindow*): References to action buttons

## Dependencies
- `GameClient/GameWindow.h`, `GameClient/GameText.h`, `GameClient/Gadget.h`, `GameClient/GadgetTextEntry.h`, `GameClient/GadgetListBox.h`, `GameClient/GameClient.h`, `GameClient/DisconnectMenu.h`, `GameClient/GameWindowManager.h`, `Common/NameKeyGenerator.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheGameText`, `TheDisconnect
