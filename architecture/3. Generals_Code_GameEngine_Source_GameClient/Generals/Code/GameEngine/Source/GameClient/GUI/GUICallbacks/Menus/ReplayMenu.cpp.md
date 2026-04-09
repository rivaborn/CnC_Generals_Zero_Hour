# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/ReplayMenu.cpp

## Purpose
Handles the replay menu UI, allowing players to view, load, delete, and copy replay files.

## Responsibilities
- Populate and manage the replay file listbox
- Handle user input for replay selection and actions
- Initialize and shutdown the replay menu
- Delete and copy replay files
- Load selected replays for playback

## Key Types
- `ReplayMenuSystem` (Function): Main system callback for replay menu events
- `PopulateReplayFileListbox` (Function): Populates the listbox with replay files
- `GetReplayFilenameFromListbox` (Function): Extracts filename from listbox selection
- `deleteReplay` (Function): Deletes selected replay file
- `copyReplay` (Function): Copies selected replay file to desktop

## Key Functions
### `ReplayMenuSystem`
- Purpose: Handles all system messages for the replay menu
- Calls: `reallyLoadReplay`, `deleteReplayFlag`, `copyReplayFlag`, `TheShell->pop()`

### `PopulateReplayFileListbox`
- Purpose: Populates the listbox with replay files and their metadata
- Calls: `TheFileSystem->getFileListInDirectory`, `TheRecorder->readReplayHeader`, `GadgetListBoxAddEntryText`

### `deleteReplay`
- Purpose: Deletes the selected replay file
- Calls: `DeleteFile`, `PopulateReplayFileListbox`

### `copyReplay`
- Purpose: Copies the selected replay file to the desktop
- Calls: `CopyFile`, `SHGetSpecialFolderLocation`, `SHGetPathFromIDList`

## Globals
- `parentReplayMenuID` (NameKeyType): ID for the parent replay menu window
- `buttonLoadID` (NameKeyType): ID for the load button
- `buttonBackID` (NameKeyType): ID for the back button
- `listboxReplayFilesID` (NameKeyType): ID for the replay files listbox
- `buttonDeleteID` (NameKeyType): ID for the delete button
- `buttonCopyID` (NameKeyType): ID for the copy button
- `isShuttingDown` (Bool): Flag indicating if the menu is shutting down
- `callCopy` (Bool): Flag to trigger copy operation
- `callDelete` (Bool): Flag to trigger delete operation

## Dependencies
- `PreRTS.h`, `Lib/BaseType.h`, `Common/FileSystem.h`, `Common/GameEngine.h`, `Common/GameState.h`, `Common/Recorder.h`, `Common/Version.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/GadgetListbox.h`, `GameClient/Shell.h`, `GameClient/KeyDefs.h`, `GameClient/GameWindowManager.h`, `GameClient/MessageBox.h`, `GameClient/MapUtil.h`, `GameClient/GameText.h`, `GameClient/GameWindowTransitions.h`
- `TheRecorder`, `TheMapCache`, `TheFileSystem`, `TheNameKeyGenerator`, `TheWindowManager`, `TheShell`, `TheTransitionHandler`, `TheGameText`, `TheGlobalData`, `TheVersion`
