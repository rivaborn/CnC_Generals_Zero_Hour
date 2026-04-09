# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLQuickMatchMenu.cpp

## Purpose
Handles the Quick Match menu UI for online multiplayer, including ladder selection, map selection, and match configuration.

## Responsibilities
- Manages Quick Match menu UI elements and their interactions
- Handles ladder selection and validation
- Configures match settings (players, ping, disconnects, etc.)
- Populates UI controls with available maps, ladders, and player options
- Processes user input for starting/stopping matches

## Key Types
- MapListboxIndex (Class): tracks map selection indices for variable map counts
- (anonymous enum): defines max disconnect limits (ANY, 5, 10, 25, 50)
- MAX_DISCONNECTS_COUNT (Enum): count of disconnect limit options

## Key Functions
### UpdateStartButton
- Purpose: Enables/disables the start button based on ladder/map selection
- Calls: GadgetComboBoxGetSelectedPos, GadgetComboBoxGetItemData, TheLadderList->findLadderByIndex, GadgetListBoxGetNumEntries, GadgetListBoxGetItemData

### populateQMColorComboBox
- Purpose: Populates the color selection combo box with available player colors
- Calls: GadgetComboBoxReset, TheMultiplayerSettings->getNumColors, TheMultiplayerSettings->getColor, GadgetComboBoxAddEntry, GadgetComboBoxSetItemData, GadgetComboBoxSetSelectedPos

### populateQMSideComboBox
- Purpose: Populates the side/faction selection combo box with available player templates
- Calls: GadgetComboBoxReset, ThePlayerTemplateStore->getPlayerTemplateCount, ThePlayerTemplateStore->getNthPlayerTemplate, GadgetComboBoxAddEntry, GadgetComboBoxSetItemData, GadgetComboBoxSetSelectedPos

### WOLQuickMatchMenuSystem
- Purpose: Main window system callback handling UI messages and events
- Calls: saveQuickMatchOptions, PopulateQMLadderComboBox, GameSpyOpenOverlay, TheGameSpyPeerMessageQueue->addRequest, GadgetComboBoxGetSelectedPos, GadgetComboBoxGetItemData, TheLadderList->findLadderByIndex, GadgetListBoxGetNumEntries, GadgetListBoxGetItemData, TheGameSpyPSMessageQueue->findPlayerStatsByID, CalculateRank, TheGameSpyInfo->getLocalProfileID, TheGameSpyConfig->getQMBotID, TheGameSpyConfig->getQMChannel, TheGlobalData->m_exeCRC, TheGlobalData->m_iniCRC, TheShell->pop

## Globals
- parentWOLQuickMatchID (NameKeyType): ID for the parent window
- buttonBackID (NameKeyType): ID for the back button
- buttonStartID (NameKeyType): ID for the start button
- buttonStopID (NameKeyType): ID for the stop button
- buttonWidenID (NameKeyType): ID for the widen search button
- buttonBuddiesID (NameKeyType): ID for the buddies button
- listboxQuickMatchID (NameKeyType): ID for the quick match list box
- listboxMapSelectID (NameKeyType): ID for the map selection list box
- buttonSelectAllMapsID (NameKeyType): ID for the select all maps button
- buttonSelectNoMapsID (NameKeyType): ID for the select no maps button
- textEntryWaitTimeID (NameKeyType): ID for the wait time text entry
- comboBoxNumPlayersID (NameKeyType): ID for the number of players combo box
- comboBoxMaxPingID (
