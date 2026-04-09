# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLMapSelectMenu.cpp

## Purpose
Handles the map selection menu UI for Westwood Online (WOL) multiplayer in Command & Conquer Generals.

## Responsibilities
- Manages map selection UI initialization and shutdown
- Handles map list population and preview display
- Processes user input for map selection and start position configuration
- Coordinates with GameSpy overlay for multiplayer game setup

## Key Types
- **None**

## Key Functions
### WOLMapSelectMenuInit
- Purpose: Initializes the map selection menu UI
- Calls: TheWindowManager->winGetWindowFromId, TheNameKeyGenerator->nameToKey, TheMapCache->updateCache, populateMapListbox

### WOLMapSelectMenuShutdown
- Purpose: Cleans up map selection menu resources
- Calls: NullifyControls, layout->hide, TheShell->shutdownComplete

### WOLMapSelectMenuInput
- Purpose: Handles keyboard input for the map selection menu
- Calls: TheWindowManager->winGetWindowFromId, TheWindowManager->winSendSystemMsg

### WOLMapSelectMenuSystem
- Purpose: Processes system messages for the map selection menu
- Calls: NullifyControls, TheWindowManager->winGetWindowFromId, TheWindowManager->winSendSystemMsg, GadgetListBoxSetSelected, GadgetListBoxGetText, GadgetListBoxGetItemData, getMapPreviewImage, positionStartSpots, TheGameSpyGame->setMap, TheGameSpyGame->setMapCRC, TheGameSpyGame->setMapSize, TheGameSpyGame->adjustSlotsForMap, TheGameSpyGame->resetAccepted, TheGameSpyGame->resetStartSpots, TheGameSpyInfo->setGameOptions, WOLDisplaySlotList, WOLDisplayGameOptions, WOLMapSelectLayout->destroyWindows, WOLMapSelectLayout->deleteInstance, WOLPositionStartSpots

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
- buttonMapStartPosition
