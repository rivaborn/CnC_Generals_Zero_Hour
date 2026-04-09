# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupHostGame.cpp

## Purpose
Handles the UI callbacks for the "Host Game" popup menu in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages initialization, update, and input handling for the host game UI
- Populates ladder lists and combo boxes with available game ladders
- Handles game creation requests and configuration preferences
- Manages observer settings, password protection, and faction limitations

## Key Types
- **None**

## Key Functions
### createGame
- Purpose: Creates a new game session with configured settings
- Calls: TheGameSpyGame->setGameName, TheGameSpyGame->setAllowObservers, TheGameSpyGame->setOldFactionsOnly, TheGameSpyGame->setUseStats, TheGameSpyGame->setLadderIP, TheGameSpyGame->setLadderPort, TheGameSpyPeerMessageQueue->addRequest

### CustomMatchHideHostPopup
- Purpose: Shows or hides the host game popup window
- Calls: parentPopup->winHide

### HandleCustomLadderSelection
- Purpose: Handles user selection of a ladder from the list
- Calls: pref.setLastLadder, pref.write

### PopulateCustomLadderListBox
- Purpose: Populates the ladder list box with available ladders
- Calls: GadgetListBoxReset, GadgetListBoxAddEntryText, GadgetListBoxSetItemData, GadgetListBoxSetSelected

### PopulateCustomLadderComboBox
- Purpose: Populates the ladder combo box with available ladders
- Calls: GadgetComboBoxReset, GadgetComboBoxAddEntry, GadgetComboBoxSetItemData, GadgetComboBoxSetSelectedPos

### PopupHostGameInit
- Purpose: Initializes the host game popup window and its controls
- Calls: TheWindowManager->winGetWindowFromId, GadgetTextEntrySetText, GadgetCheckBoxSetChecked, PopulateCustomLadderComboBox, TheWindowManager->winSetFocus, TheWindowManager->winSetModal

### PopupHostGameUpdate
- Purpose: Updates the host game popup based on current settings
- Calls: GadgetCheckBoxIsChecked, checkBoxLimitArmies->winEnable, GadgetCheckBoxSetChecked

### PopupHostGameInput
- Purpose: Handles keyboard input for the host game popup
- Calls: TheWindowManager->winSendSystemMsg

### PopupHostGameSystem
- Purpose: Handles system messages for the host game popup
- Calls: GadgetTextEntryGetText, GadgetTextEntrySetText, GadgetComboBoxGetSelectedPos, GadgetComboBoxGetItemData, GameSpyOpenOverlay, GameSpyCloseOverlay, SetLobbyAttemptHostJoin

## Globals
- parentPopupID (NameKeyType): ID for the parent popup window
- textEntryGameNameID (NameKeyType): ID for the game name text entry
- buttonCreateGameID (NameKeyType): ID for the create game button
- checkBoxAllowObserversID (NameKeyType): ID for the allow observers checkbox
- textEntryGameDescriptionID (NameKeyType): ID for the game description text entry
- buttonCancelID (NameKeyType): ID for the cancel button
- textEntryLadderPasswordID (NameKeyType): ID for the ladder password text entry
- comboBoxLadderNameID (NameKeyType): ID for the ladder name combo box
- textEntryGamePasswordID (NameKeyType): ID for the game password text entry
- checkBoxLimitArmiesID (NameKeyType): ID for the limit armies checkbox
- checkBoxUseStatsID (
