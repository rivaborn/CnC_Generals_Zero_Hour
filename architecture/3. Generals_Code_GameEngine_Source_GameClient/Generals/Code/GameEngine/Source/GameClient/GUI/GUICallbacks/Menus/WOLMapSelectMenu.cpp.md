# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLMapSelectMenu.cpp

## Purpose
Handles the map selection menu UI for GameSpy multiplayer matches in Command & Conquer Generals.

## Responsibilities
- Manages map selection UI initialization and shutdown
- Handles user input for map selection and start position placement
- Updates map preview and list based on system/user maps
- Coordinates with GameSpy game options and slot management

## Key Types
- **None**

## Key Functions
### WOLMapSelectMenuInit
- Purpose: Initializes the map selection menu UI
- Calls: TheWindowManager->winGetWindowFromId, TheNameKeyGenerator->nameToKey, GadgetRadioSetSelection, TheMapCache->updateCache, populateMapListbox

### WOLMapSelectMenuShutdown
- Purpose: Cleans up map selection menu resources
- Calls: NullifyControls, layout->hide, TheShell->shutdownComplete

### WOLMapSelectMenuInput
- Purpose: Handles keyboard input for the map selection menu
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winSendSystemMsg

### WOLMapSelectMenuSystem
- Purpose: Processes system messages for the map selection menu
- Calls: NullifyControls, showGameSpyGameOptionsUnderlyingGUIElements, WOLMapSelectLayout->destroyWindows, WOLMapSelectLayout->deleteInstance, WOLPositionStartSpots, TheMapCache->updateCache, populateMapListbox, CustomMatchPreferences::setUsesSystemMapDir, CustomMatchPreferences::write, TheGameSpyGame->setMap, TheGameSpyGame->setMapCRC, TheGameSpyGame->setMapSize, TheGameSpyGame->adjustSlotsForMap, TheGameSpyGame->resetAccepted, TheGameSpyGame->resetStartSpots, TheGameSpyInfo->setGameOptions, WOLDisplaySlotList, WOLDisplayGameOptions

## Globals
- buttonBack (NameKeyType): ID for the back button
- buttonOK (NameKeyType): ID for the OK button
- listboxMap (NameKeyType): ID for the map listbox
- parent (GameWindow*): Parent window reference
- raiseMessageBoxes (Bool): Flag for message box handling
- winMapPreview (GameWindow*): Map preview window
- winMapPreviewID (NameKeyType): ID for map preview window
- radioButtonSystemMapsID (NameKeyType): ID for system maps radio button
- radioButtonUserMapsID (NameKeyType): ID for user maps radio button
- WOLMapSelectLayout (WindowLayout*): Map selection overlay layout
- mapList (GameWindow*): Map list window
- buttonMapStartPosition (GameWindow*[]): Start position buttons for
