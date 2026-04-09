# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DisconnectWindow.cpp

## Purpose
Manages the in-game disconnect menu UI for network games, including chat and player voting.

## Responsibilities
- Initializes and displays the disconnect menu window
- Handles user input for chat and player voting
- Manages menu visibility and control states
- Interfaces with network game management systems

## Key Types
- **None**

## Key Functions
### InitDisconnectWindow
- Purpose: Initializes UI elements and retrieves window references
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetTextEntrySetText, TheWindowManager->winSetFocus

### ShowDisconnectWindow
- Purpose: Displays the disconnect menu and configures controls based on game state
- Calls: TheWindowManager->winCreateLayout, InitDisconnectWindow, disconnectMenuLayout->hide, buttonVotePlayerXWindow->winEnable, buttonQuitWindow->winEnable, disconnectMenuLayout->bringForward, GadgetListBoxReset, GadgetListBoxAddEntryText

### HideDisconnectWindow
- Purpose: Hides the disconnect menu
- Calls: TheWindowManager->winCreateLayout, InitDisconnectWindow, disconnectMenuLayout->hide

### DisconnectControlInput
- Purpose: Handles input messages for the disconnect menu
- Calls: None

### DisconnectControlSystem
- Purpose: Processes system messages for menu controls (button clicks, text entry)
- Calls: TheDisconnectMenu->quitGame, TheDisconnectMenu->voteForPlayer, GadgetTextEntryGetText, TheDisconnectMenu->sendChat

## Globals
- disconnectMenuLayout (WindowLayout*): Stores the menu layout reference
- textEntryID/textDisplayID (NameKeyType): IDs for text input/output controls
- textEntryWindow/textDisplayWindow (GameWindow*): Pointers to text controls
- buttonQuitID/buttonQuitWindow (NameKeyType/GameWindow*): Quit button references
- buttonVotePlayerXID/buttonVotePlayerXWindow (NameKeyType/GameWindow*): Voting button references (1-7)

## Dependencies
- GameClient headers (GameWindow, GameText, Gadget, GadgetTextEntry, GadgetListBox, GameClient, DisconnectMenu, GameWindowManager)
- Common/NameKeyGenerator.h
- GameNetwork/GameInfo.h
