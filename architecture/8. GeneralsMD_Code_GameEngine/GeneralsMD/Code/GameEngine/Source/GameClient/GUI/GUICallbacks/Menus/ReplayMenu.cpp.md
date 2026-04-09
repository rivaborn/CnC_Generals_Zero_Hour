# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ReplayMenu.cpp

## Purpose
Handles the replay menu UI, allowing players to view, load, delete, and copy replay files.

## Responsibilities
- Populate and manage the replay file listbox
- Handle user input for replay operations (load/delete/copy)
- Initialize and shutdown the replay menu
- Display replay metadata (name, date, version, map)
- Manage replay file operations (deletion/copying)

## Key Types
- `ReplayMenuSystem` (Function): Main window system callback for replay menu
- `PopulateReplayFileListbox` (Function): Populates listbox with replay files
- `GetReplayFilenameFromListbox` (Function): Extracts filename from selected listbox item
- `RecorderClass::ReplayHeader` (Struct): Contains replay header information
- `ReplayGameInfo` (Struct): Contains parsed game info from replay

## Key Functions
### `ReplayMenuSystem`
- Purpose: Handles window system messages for the replay menu
- Calls: `reallyLoadReplay`, `deleteReplayFlag`, `copyReplayFlag`, `MessageBoxOk`, `MessageBoxYesNo`

### `PopulateReplayFileListbox`
- Purpose: Populates the listbox with available replay files and their metadata
- Calls: `GadgetListBoxReset`, `TheFileSystem->getFileListInDirectory`, `TheRecorder->readReplayHeader`, `GadgetListBoxAddEntryText`

### `deleteReplay`
- Purpose: Deletes the selected replay file
- Calls: `GadgetListBoxGetSelected`, `GetReplayFilenameFromListbox`, `DeleteFile`, `MessageBoxOk`

### `copyReplay`
- Purpose: Copies the selected replay file to the desktop
- Calls: `GadgetListBoxGetSelected`, `GetReplayFilenameFromListbox`, `CopyFile`, `MessageBoxOk`

## Globals
- `parentReplayMenuID` (NameKeyType): ID for the parent replay menu window
- `listboxReplayFilesID` (NameKeyType): ID for the replay files listbox
- `isShuttingDown` (Bool): Flag indicating if the menu is shutting down
- `parentReplayMenu` (GameWindow*): Pointer to the parent replay menu window
- `listboxReplayFiles` (GameWindow*): Pointer to the replay files listbox
- `callCopy` (Bool): Flag to trigger replay copying
- `callDelete` (Bool): Flag to trigger replay deletion

## Dependencies
- `Recorder.h` (TheRecorder): For replay file operations
- `GadgetListbox.h` (GadgetListBox functions): For listbox management
- `MessageBox.h` (MessageBox functions): For user confirmation dialogs
- `MapUtil.h` (TheMapCache): For map metadata
- `GameText.h` (TheGameText): For localized text strings
- Windows API (SHGetSpecialFolderLocation, CopyFile, DeleteFile): For file operations
