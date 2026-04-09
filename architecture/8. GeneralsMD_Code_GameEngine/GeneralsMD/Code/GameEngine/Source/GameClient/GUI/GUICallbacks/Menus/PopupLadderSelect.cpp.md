# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupLadderSelect.cpp

## Purpose
Handles the ladder selection popup UI in Command & Conquer Generals Zero Hour, including password entry and ladder details display.

## Responsibilities
- Manages ladder selection UI initialization and input handling
- Handles password entry for protected ladders
- Displays ladder details (name, location, maps, factions, etc.)
- Populates ladder lists and combo boxes
- Manages right-click ladder details menus

## Key Types
- **PasswordMode (Enum)**: Tracks password entry state (none, entry, error)
- **PASS_NONE (Enum)**: No password mode active
- **PASS_ENTRY (Enum)**: Password entry mode active
- **PASS_ERROR (Enum)**: Password error mode active

## Key Functions
### `PopupLadderSelectInit`
- Purpose: Initializes the ladder selection popup UI
- Calls: `setPasswordMode`, `populateLadderListBox`, `CustomMatchHideHostPopup`

### `PopupLadderSelectInput`
- Purpose: Handles keyboard input for the ladder selection popup
- Calls: `setPasswordMode`, `populateLadderComboBox`, `GameSpyCloseOverlay`

### `PopupLadderSelectSystem`
- Purpose: Handles system messages for the ladder selection popup
- Calls: `updateLadderDetails`, `setPasswordMode`, `ladderSelectedCallback`, `GameSpyCloseOverlay`

### `updateLadderDetails`
- Purpose: Updates the ladder details display with information about the selected ladder
- Calls: `GadgetStaticTextSetText`, `GadgetListBoxReset`, `GadgetListBoxAddEntryText`, `TheGameText->fetch`

### `setPasswordMode`
- Purpose: Manages the password entry UI state
- Calls: `winHide`, `winEnable`, `GadgetTextEntrySetText`, `TheWindowManager->winSetFocus`

## Globals
- **parentID (NameKeyType)**: ID for the parent window
- **listboxLadderSelectID (NameKeyType)**: ID for the ladder selection listbox
- **listboxLadderDetailsID (NameKeyType)**: ID for the ladder details listbox
- **staticTextLadderNameID (NameKeyType)**: ID for the ladder name static text
- **buttonOkID (NameKeyType)**: ID for the OK button
- **buttonCancelID (NameKeyType)**: ID for the cancel button
- **passwordParentID (NameKeyType)**: ID for the password entry parent window
- **buttonPasswordOkID (NameKeyType)**: ID for the password OK button
- **buttonPasswordCancelID (NameKeyType)**: ID for the password cancel button
- **textEntryPasswordID (NameKeyType)**: ID for the password text entry
- **badPasswordParentID (NameKeyType)**: ID for the bad password parent window
- **buttonBadPasswordOkID (NameKeyType)**: ID for the bad password OK button
- **s_currentMode (PasswordMode)**: Current password mode state
- **ladderIndex (Int)**: Index of the currently selected ladder

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `Common/Encrypt.h`, `Common/NameKeyGenerator.h`
- `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/GameText.h`
- `GameClient/KeyDefs.h`, `GameClient/MapUtil.h`, `GameClient/GadgetListBox.h`
- `GameClient/GadgetStaticText.h`, `GameClient/GadgetTextEntry.h`
- `GameNetwork/GameSpy/LadderDefs.h`, `GameNetwork/GameSpy/Peer
