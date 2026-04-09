# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupSaveLoad.cpp

## Purpose
Handles the save/load game menu UI, including initialization, input processing, and game save/load operations.

## Responsibilities
- Manages save/load menu UI state and transitions
- Handles user input for save/load/delete operations
- Populates and updates the save game listbox
- Coordinates game save/load actions with the game state

## Key Types
- `SaveLoadLayoutType` (Enum): Defines menu modes (save/load, load-only, save-only)
- `AvailableGameInfo` (Struct): Contains save game metadata
- `GameWindow` (Class): UI window handle

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
- Calls: `processLoadButtonPress`, `closeSaveMenu`, `doLoadGame`, `updateMenuActions`

### `doLoadGame`
- Purpose: Loads the selected save game
- Calls: `getSelectedSaveFileInfo`, `destroyQuitMenu`, `prepareNewGame`

## Globals
- `buttonBackKey` (NameKeyType): ID for back button
- `listboxGamesKey` (NameKeyType): ID for games listbox
- `currentLayoutType` (SaveLoadLayoutType): Current menu mode
- `isPopup` (Bool): Whether menu is popup or full-screen
- `parent` (GameWindow*): Parent window handle

## Dependencies
- `GameEngine.h`, `GameState.h`, `CampaignManager.h`, `GadgetListBox.h`
- `GameWindowManager.h`, `GUICallbacks.h`, `Shell.h`, `GameLogic.h`
- `GameWindowTransitions.h`
