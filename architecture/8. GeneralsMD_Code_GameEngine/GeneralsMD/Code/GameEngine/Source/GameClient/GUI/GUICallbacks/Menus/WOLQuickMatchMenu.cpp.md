# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLQuickMatchMenu.cpp

## Purpose
Handles the Quick Match menu UI for online multiplayer, including ladder selection, map selection, and game options.

## Responsibilities
- Manages Quick Match menu initialization and shutdown
- Handles UI input and system messages for the menu
- Populates and updates combo boxes and list boxes with game options
- Validates ladder selection based on player stats
- Saves and applies Quick Match preferences

## Key Types
- (anonymous enum): Defines max disconnect limits (0, 5, 10, 25, 50)
- MAX_DISCONNECTS_COUNT (Enum): Count of disconnect limit options (5)

## Key Functions
### UpdateStartButton
- Purpose: Enables/disables the start button based on ladder/map selection
- Calls: GadgetComboBoxGetSelectedPos, GadgetComboBoxGetItemData, TheLadderList->findLadderByIndex, GadgetListBoxGetNumEntries, GadgetListBoxGetItemData

### populateQMColorComboBox
- Purpose: Populates the color selection combo box with available player colors
- Calls: TheMultiplayerSettings->getNumColors, TheMultiplayerSettings->getColor, TheGameText->fetch, GadgetComboBoxReset, GadgetComboBoxAddEntry, GadgetComboBoxSetItemData, GadgetComboBoxSetSelectedPos

### populateQMSideComboBox
- Purpose: Populates the side/faction selection combo box with valid options
- Calls: ThePlayerTemplateStore->getPlayerTemplateCount, ThePlayerTemplateStore->getNthPlayerTemplate, TheGameText->fetch, GadgetComboBoxReset, GadgetComboBoxAddEntry, GadgetComboBoxSetItemData, GadgetComboBoxSetSelectedPos

### HandleQMLadderSelection
- Purpose: Handles ladder selection changes and saves preferences
- Calls: QuickMatchPreferences::setLastLadder, QuickMatchPreferences::write, TheLadderList->findLadderByIndex

### isValidLadder
- Purpose: Checks if a ladder is valid based on player win/loss stats
- Calls: TheGameSpyPSMessageQueue->findPlayerStatsByID, TheGameSpyInfo->getLocalProfileID

### PopulateQMLadderListBox
- Purpose: Populates the ladder selection list box with available ladders
- Calls: TheLadderList->getLadderCount, TheLadderList->getNthLadder, TheGameText->fetch, GadgetListBoxReset, GadgetListBoxAddEntry, GadgetListBoxSetItemData

### saveQuickMatchOptions
- Purpose: Saves current Quick Match options to preferences
- Calls: QuickMatchPreferences::loadProfile, QuickMatchPreferences::setNumPlayers, QuickMatchPreferences::setSide, QuickMatchPreferences::setColor, QuickMatchPreferences::setMaxPing, QuickMatchPreferences::setMaxDisconnects, QuickMatchPreferences::setWaitTime, QuickMatchPreferences::setLastLadder, QuickMatchPreferences::write

### WOLQuickMatchMenuInit
- Purpose: Initializes the Quick Match menu UI
- Calls: TheWindowManager->winGetWindowFromId, TheWindowManager->winGetWindowId, TheWindowManager->winGetWindow, TheWindowManager->winGetWindowId, TheWindowManager->winGetWindow, TheWindowManager->winGetWindowId, TheWindowManager->winGetWindow, TheWindowManager->winGetWindowId, TheWindowManager->winGetWindow, TheWindowManager->winGetWindowId, TheWindowManager->winGetWindow, TheWindowManager->winGetWindowId, TheWindowManager->win
