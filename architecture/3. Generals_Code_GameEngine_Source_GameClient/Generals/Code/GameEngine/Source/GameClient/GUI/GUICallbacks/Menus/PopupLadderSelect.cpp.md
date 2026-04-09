# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupLadderSelect.cpp

## Purpose
Handles UI callbacks for the ladder selection popup in Command & Conquer Generals.

## Responsibilities
- Manages ladder selection UI elements (list boxes, buttons, text fields)
- Handles password entry for protected ladders
- Populates and updates ladder details display
- Processes user input for ladder selection
- Manages right-click ladder details menu

## Key Types
- **PasswordMode (Enum)**: Tracks password entry state (none, entry, error)
- **PASS_NONE (Enum)**: No password mode
- **PASS_ENTRY (Enum)**: Password entry mode
- **PASS_ERROR (Enum)**: Password error mode

## Key Functions
### PopupLadderSelectInit
- Purpose: Initializes the ladder selection popup UI
- Calls: `TheWindowManager->winGetWindowFromId`, `setPasswordMode`, `populateLadderListBox`, `CustomMatchHideHostPopup`

### PopupLadderSelectInput
- Purpose: Handles keyboard input for the ladder selection popup
- Calls: `setPasswordMode`, `populateLadderComboBox`, `GameSpyCloseOverlay`

### PopupLadderSelectSystem
- Purpose: Handles system messages for the ladder selection popup
- Calls: `GadgetListBoxGetSelected`, `updateLadderDetails`, `handleLadderSelection`, `populateLadderComboBox`, `GameSpyCloseOverlay`, `setPasswordMode`, `EncryptString`

### updateLadderDetails
- Purpose: Updates the ladder details display with selected ladder information
- Calls: `GadgetStaticTextSetText`, `GadgetListBoxReset`, `TheLadderList->findLadderByIndex`, `GadgetListBoxAddEntryText`, `TheGameText->fetch`, `TheMapCache->findMap`

### setPasswordMode
- Purpose: Manages password entry UI state transitions
- Calls: `winHide`, `winEnable`, `GadgetTextEntrySetText`, `TheWindowManager->winSetFocus`

## Globals
- **parentID (NameKeyType)**: ID for the parent window
- **listboxLadderSelectID (NameKeyType)**: ID for the ladder selection list box
- **listboxLadderDetailsID (NameKeyType)**: ID for the ladder details list box
- **staticTextLadderNameID (NameKeyType)**: ID for the ladder name text
- **buttonOkID (NameKeyType)**: ID for the OK button
- **buttonCancelID (NameKeyType)**: ID for the cancel button
- **passwordParentID (NameKeyType)**: ID for the password entry parent
- **buttonPasswordOkID (NameKeyType)**: ID for the password OK button
- **buttonPasswordCancelID (NameKeyType)**: ID for the password cancel button
- **textEntryPasswordID (NameKeyType)**: ID for the password text entry
- **badPasswordParentID (NameKeyType)**: ID for the bad password parent
- **buttonBadPasswordOkID (NameKeyType)**: ID for the bad password OK button
- **s_currentMode (PasswordMode)**: Current password mode state
- **ladderIndex (Int)**: Index of the currently selected ladder

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `Common/Encrypt.h`, `Common/NameKeyGenerator.h`
- `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/GameText.h`
- `GameClient/KeyDefs.h`, `GameClient/MapUtil.h`, `GameClient/GadgetListBox.h`
- `GameClient/GadgetStaticText.h`, `GameClient
