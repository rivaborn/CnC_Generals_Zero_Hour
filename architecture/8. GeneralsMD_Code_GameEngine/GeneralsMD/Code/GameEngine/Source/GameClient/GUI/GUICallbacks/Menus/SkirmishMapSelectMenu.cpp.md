# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SkirmishMapSelectMenu.cpp

## Purpose
Handles the skirmish map selection menu UI, including map list population, preview display, and start position management.

## Responsibilities
- Manages map selection UI elements (listbox, preview, buttons)
- Populates map list based on system/user maps
- Handles map preview display and start position buttons
- Processes user input (selection, navigation, radio button toggles)
- Updates global skirmish game info with selected map

## Key Types
- **None** (file contains only functions and globals)

## Key Functions
### NullifyControls
- Purpose: Resets all UI control pointers to NULL
- Calls: None

### mapListTooltipFunc
- Purpose: Sets tooltip text for map list entries based on difficulty
- Calls: `GadgetListBoxGetEntryBasedOnXY`, `GadgetListBoxGetItemData`, `TheMouse->setCursorTooltip`

### showSkirmishGameOptionsUnderlyingGUIElements
- Purpose: Shows/hides underlying game options UI elements
- Calls: `TheWindowManager->winGetWindowFromId`, `GameWindow::winHide`, `GameWindow::winEnable`

### SkirmishMapSelectMenuInit
- Purpose: Initializes the map selection menu UI
- Calls: `TheWindowManager->winGetWindowFromId`, `GadgetRadioSetSelection`, `populateMapListbox`, `TheMapCache->updateCache`

### SkirmishMapSelectMenuInput
- Purpose: Handles keyboard input for the map selection menu
- Calls: `TheWindowManager->winSendSystemMsg`

### SkirmishMapSelectMenuSystem
- Purpose: Processes system messages for the map selection menu
- Calls: `GadgetListBoxSetSelected`, `GadgetListBoxGetText`, `GadgetListBoxGetItemData`, `getMapPreviewImage`, `positionStartSpots`, `TheSkirmishGameInfo->setMap`

## Globals
- `buttonBack` (NameKeyType): ID for back button
- `buttonOK` (NameKeyType): ID for OK button
- `listboxMap` (NameKeyType): ID for map listbox
- `parent` (GameWindow*): Parent window pointer
- `mapList` (GameWindow*): Map list window pointer
- `radioButtonSystemMapsID` (NameKeyType): ID for system maps radio button
- `radioButtonUserMapsID` (NameKeyType): ID for user maps radio button
- `buttonMapStartPosition` (GameWindow*[]): Array of start position buttons
- `buttonMapStartPositionID` (NameKeyType[]): Array of start position button IDs
- `winMapPreview` (GameWindow*): Map preview window pointer
- `winMapPreviewID` (NameKeyType): ID for map preview window
- `skirmishMapSelectLayout` (WindowLayout*): Layout for skirmish map selection

## Dependencies
- `PreRTS.h`, `GameEngine.h`, `MessageStream.h`, `UserPreferences.h`, `WindowLayout.h`, `Gadget.h`, `GameText.h`, `Mouse.h`, `Shell.h`, `GameWindowManager.h`, `GadgetListBox.h`, `GadgetRadioButton.h`, `GadgetStaticText.h`, `LANAPICallbacks.h`, `MapUtil.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheMouse`, `TheGameText`, `TheMapCache`, `TheShell`, `TheSkirmishGameInfo`
