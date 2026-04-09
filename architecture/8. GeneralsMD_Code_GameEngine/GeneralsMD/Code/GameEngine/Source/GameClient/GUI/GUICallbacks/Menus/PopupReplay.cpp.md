# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupReplay.cpp

## Purpose
Handles the replay save/load menu UI and functionality in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages the replay save/load menu initialization and shutdown
- Handles user input for replay saving
- Displays confirmation popups for saved replays
- Manages file operations for replay saving
- Updates UI controls based on user actions

## Key Types
- **NameKeyType** (Type): Used for identifying UI elements
- **GameWindow** (Class): Base class for UI windows
- **WindowLayout** (Class): UI layout manager
- **UnicodeString** (Class): Unicode string handling
- **AsciiString** (Class): ASCII string handling

## Key Functions
### PopupReplayInit
- Purpose: Initializes the replay save/load menu
- Calls: TheWindowManager->winGetWindowFromId, PopulateReplayFileListbox, GadgetTextEntrySetText, TheWindowManager->winSetFocus

### PopupReplaySystem
- Purpose: Handles system messages for the replay menu
- Calls: TheWindowManager->winGetWindowFromId, GadgetListBoxGetText, GadgetTextEntryGetText, saveReplay, closeSaveMenu, ScoreScreenEnableControls

### saveReplay
- Purpose: Initiates the replay saving process
- Calls: TheRecorder->getReplayDir, TheRecorder->getReplayExtention, TheLocalFileSystem->doesFileExist, MessageBoxOkCancel, reallySaveReplay

### reallySaveReplay
- Purpose: Performs the actual replay file operations
- Calls: TheRecorder->getReplayDir, TheRecorder->getReplayExtention, TheLocalFileSystem->doesFileExist, DeleteFile, CopyFile, PopulateReplayFileListbox, ShowReplaySavedPopup

## Globals
- **buttonBackKey** (NameKeyType): ID for the back button
- **buttonSaveKey** (NameKeyType): ID for the save button
- **listboxGamesKey** (NameKeyType): ID for the games listbox
- **textEntryReplayNameKey** (NameKeyType): ID for the replay name text entry
- **parent** (GameWindow*): Pointer to the main menu window
- **replaySavedParent** (GameWindow*): Pointer to the replay saved popup window
- **s_fileSavePopupStartTime** (time_t): Timer for the replay saved popup
- **s_fileSavePopupDuration** (time_t): Duration for the replay saved popup
- **LastReplayFileName** (std::string): Last replay filename
- **replayPath** (std::string): Path for the replay being
