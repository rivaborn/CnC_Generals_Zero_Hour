# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishMapSelectMenu.cpp

## Purpose
Handles the skirmish map selection menu UI, including map list population, preview display, and start position management.

## Responsibilities
- Manages map listbox population and filtering (system/user maps)
- Handles map preview rendering and start position buttons
- Processes user input (selection, navigation, radio button toggles)
- Updates global skirmish game info with selected map
- Coordinates with underlying game options menu

## Key Types
- **None**

## Key Functions
### NullifyControls
- Purpose: Resets all UI control pointers to NULL
- Calls: None

### mapListTooltipFunc
- Purpose: Sets tooltip text for map list entries based on difficulty
- Calls: `GadgetListBoxGetEntryBasedOnXY`, `GadgetListBoxGetItemData`, `TheMouse->setCursorTooltip`

### showSkirmishGameOptionsUnderlyingGUIElements
- Purpose: Shows/hides underlying game options menu elements
- Calls: `TheWindowManager->winGetWindowFromId`, `GameWindow::winHide`, `GameWindow::winEnable`

### SkirmishMapSelectMenuInit
- Purpose: Initializes the map selection menu UI
- Calls: `TheWindowManager->winGetWindowFromId`, `GadgetRadioSetSelection`, `populateMapListbox`, `populateMapListboxNoReset`, `TheMapCache->updateCache`

### SkirmishMapSelectMenuShutdown
- Purpose: Cleans up menu resources
- Calls: `NullifyControls`, `TheShell->shutdownComplete`

### SkirmishMapSelectMenuInput
- Purpose: Handles keyboard input for the menu
- Calls: `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSendSystemMsg`

### SkirmishMapSelectMenuSystem
- Purpose: Processes window system messages
- Calls: `GadgetListBoxSetSelected`, `TheWindowManager->winSendSystemMsg`, `GadgetListBoxGetText`, `GadgetListBoxGetItemData`, `getMapPreviewImage`, `positionStartSpots`, `TheSkirmishGameInfo->setMap`, `TheSkirmishGameInfo->setMapCRC`, `TheSkirmishGameInfo->setMapSize`, `GadgetStaticTextSetText`, `skirmishPositionStartSpots`, `skirmishUpdateSlotList`

## Globals
- `buttonBack` (NameKeyType): Back button name key
- `buttonOK` (NameKeyType): OK button name key
- `listboxMap` (NameKeyType): Map listbox name key
- `parent` (GameWindow*): Parent window pointer
- `mapList` (GameWindow*): Map listbox window pointer
- `radioButtonSystemMapsID` (NameKeyType): System maps radio button name key
- `radioButtonUserMapsID` (NameKeyType): User maps radio button name key
- `buttonMapStartPosition` (GameWindow*[]): Start position buttons array
- `buttonMapStartPositionID` (NameKeyType[]): Start position buttons name keys
- `winMapPreview` (GameWindow*): Map preview window pointer
- `winMapPreviewID` (NameKeyType): Map preview window name key
- `skirmishMapSelectLayout` (WindowLayout*): Menu layout pointer

## Dependencies
- `PreRTS.h`, `GameEngine.h`, `MessageStream.h`, `UserPreferences.h`, `WindowLayout.h`, `Gadget.h`, `GameText.h`, `Mouse.h`, `Shell.h`, `GameWindow
