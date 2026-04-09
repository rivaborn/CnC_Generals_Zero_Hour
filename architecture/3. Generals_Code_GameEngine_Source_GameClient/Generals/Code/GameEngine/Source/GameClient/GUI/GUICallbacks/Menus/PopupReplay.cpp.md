# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupReplay.cpp

## Purpose
Handles the replay save/load menu UI and functionality in Command & Conquer Generals.

## Responsibilities
- Manages replay save/load UI initialization and shutdown
- Handles user input for replay naming and saving
- Displays confirmation popups for saved replays
- Manages file existence checks and overwrite confirmations
- Updates UI state based on user actions

## Key Types
- **PopupReplaySystem** (Function): Main system callback for the replay menu
- **reallySaveReplay** (Function): Handles actual replay file saving
- **saveReplay** (Function): Prepares replay file for saving with overwrite checks
- **ShowReplaySavedPopup** (Function): Controls visibility of replay saved confirmation
- **closeSaveMenu** (Function): Closes the save/load menu

## Key Functions
### PopupReplayInit
- Purpose: Initializes the replay save/load menu UI
- Calls: `TheWindowManager->winGetWindowFromId`, `PopulateReplayFileListbox`, `GadgetTextEntrySetText`, `TheWindowManager->winSetFocus`

### PopupReplaySystem
- Purpose: Handles system messages for the replay menu
- Calls: `TheWindowManager->winGetWindowFromId`, `GadgetListBoxGetText`, `GadgetTextEntrySetText`, `saveReplay`, `closeSaveMenu`, `ScoreScreenEnableControls`

### reallySaveReplay
- Purpose: Performs the actual replay file save operation
- Calls: `TheLocalFileSystem->doesFileExist`, `DeleteFile`, `CopyFile`, `PopulateReplayFileListbox`, `ShowReplaySavedPopup`

### saveReplay
- Purpose: Prepares replay file for saving with overwrite confirmation
- Calls: `TheRecorder->getReplayDir`, `TheRecorder->getReplayExtention`, `TheLocalFileSystem->doesFileExist`, `MessageBoxOkCancel`, `reallySaveReplay`

## Globals
- **buttonBackKey** (NameKeyType): ID for the back button
- **buttonSaveKey** (NameKeyType): ID for the save button
- **listboxGamesKey** (NameKeyType): ID for the games listbox
- **textEntryReplayNameKey** (NameKeyType): ID for the replay name text entry
- **parent** (GameWindow*): Pointer to the main menu window
- **replaySavedParent** (GameWindow*): Pointer to the replay saved popup window
- **s_fileSavePopupStartTime** (time_t): Timer for replay saved popup display
- **s_fileSavePopupDuration** (time_t): Duration for replay saved popup display
