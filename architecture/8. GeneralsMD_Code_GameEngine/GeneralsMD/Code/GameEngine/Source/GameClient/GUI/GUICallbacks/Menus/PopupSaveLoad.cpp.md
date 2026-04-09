# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupSaveLoad.cpp

## Purpose
Handles the save/load game menu UI, including initialization, input processing, and game save/load operations.

## Responsibilities
- Manages save/load menu UI state and transitions
- Handles user input for save/load/delete operations
- Coordinates with game state for saving/loading games
- Manages confirmation dialogs for overwrite/delete actions
- Updates UI controls based on selection and menu mode

## Key Types
- `SaveLoadLayoutType` (Enum): Defines menu modes (save/load only, save only, etc.)
- `AvailableGameInfo` (Struct): Contains save game metadata
- `SaveFileType` (Enum): Differentiates between normal and mission saves

## Key Functions
### `updateMenuActions`
- Purpose: Enables/disables menu buttons based on current selection and layout type
- Calls: `GadgetListBoxGetSelected`, `GadgetListBoxGetItemData`, `winEnable`

### `SaveLoadMenuInit`
- Purpose: Initializes the popup save/load menu
- Calls: `winGetWindowFromId`, `winSetFocus`, `winSetModal`, `populateSaveGameListbox`

### `SaveLoadMenuFullScreenInit`
- Purpose: Initializes the full-screen save/load menu
- Calls: `showShellMap`, `winGetWindowFromId`, `populateSaveGameListbox`

### `SaveLoadMenuSystem`
- Purpose: Handles system messages for the save/load menu
- Calls: `processLoadButtonPress`, `setEditDescription`, `closeSaveMenu`, `doLoadGame`, `saveGame`

### `doLoadGame`
- Purpose: Loads the selected save game
- Calls: `getSelectedSaveFileInfo`, `destroyQuitMenu`, `loadGame`

### `closeSaveMenu`
- Purpose: Closes the save/load menu
- Calls: `winSendSystemMsg`, `shutdownComplete`

## Globals
- `buttonBackKey` (NameKeyType): ID for back button
- `buttonSaveKey` (NameKeyType): ID for save button
- `buttonLoadKey` (NameKeyType): ID for load button
- `buttonDeleteKey` (NameKeyType): ID for delete button
- `listboxGamesKey` (NameKeyType): ID for games listbox
- `currentLayoutType` (SaveLoadLayoutType): Current menu mode
- `isPopup` (Bool): Whether menu is popup or fullscreen
- `parent` (GameWindow*): Parent window reference

## Dependencies
- `GameEngine.h`, `GameState.h`, `CampaignManager.h`, `GadgetListBox.h`, `GadgetTextEntry.h`, `GameText.h`, `GameWindowManager.h`, `GUICallbacks.h`, `Shell.h`, `GameLogic.h`, `GameWindowTransitions.h`
- `TheWindowManager`, `TheGameState`, `TheShell`, `TheTransitionHandler`, `TheNameKeyGenerator`
