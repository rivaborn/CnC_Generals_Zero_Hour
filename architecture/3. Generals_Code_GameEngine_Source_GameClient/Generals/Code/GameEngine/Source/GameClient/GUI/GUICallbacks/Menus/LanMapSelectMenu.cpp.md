# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanMapSelectMenu.cpp

## Purpose
Handles the LAN map selection menu UI, including map list population, preview display, and start position management.

## Responsibilities
- Initialize and shutdown the map selection menu
- Handle user input (keyboard/mouse) for map selection
- Manage map list display and filtering (system/user maps)
- Display map previews and start position buttons
- Coordinate with underlying LAN game options UI

## Key Types
- **None**

## Key Functions
### LanMapSelectMenuInit
- Purpose: Initializes the map selection menu UI and populates the map list
- Calls: `showLANGameOptionsUnderlyingGUIElements`, `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `GadgetRadioSetSelection`, `TheMapCache->updateCache`, `populateMapListbox`

### LanMapSelectMenuSystem
- Purpose: Handles system messages for the map selection menu
- Calls: `NullifyControls`, `GadgetListBoxSetSelected`, `TheWindowManager->winSendSystemMsg`, `GadgetListBoxGetSelected`, `GadgetListBoxGetText`, `GadgetListBoxGetItemData`, `TheLAN->GetMyGame()->setMap`, `TheMapCache->find`, `TheLAN->GetMyGame()->setMapCRC`, `TheLAN->GetMyGame()->setMapSize`, `TheLAN->GetMyGame()->resetStartSpots`, `TheLAN->GetMyGame()->adjustSlotsForMap`, `getMapPreviewImage`, `winMapPreview->winSetUserData`, `winMapPreview->winSetEnabledImage`, `positionStartSpots`

### LanMapSelectMenuInput
- Purpose: Handles keyboard input for the map selection menu
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSendSystemMsg`

## Globals
- `buttonBack` (NameKeyType): ID for the back button
- `buttonOK` (NameKeyType): ID for the OK button
- `listboxMap` (NameKeyType): ID for the map listbox
- `winMapPreviewID` (NameKeyType): ID for the map preview window
- `parent` (GameWindow*): Pointer to the parent window
- `mapList` (GameWindow*): Pointer to the map list window
- `winMapPreview` (GameWindow*): Pointer to the map preview window
- `radioButtonSystemMapsID` (NameKeyType): ID for the system maps radio button
- `radioButtonUserMapsID` (NameKeyType): ID for the user maps radio button
- `
