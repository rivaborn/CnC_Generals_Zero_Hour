# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/MapSelectMenu.cpp

## Purpose
Handles the map selection menu UI, including map list population, difficulty settings, and game startup.

## Responsibilities
- Initialize and shutdown the map selection menu
- Handle user input for map selection and difficulty settings
- Manage map list population based on system/user maps and solo/multiplayer modes
- Trigger game startup with selected map and difficulty

## Key Types
- **None**

## Key Functions
### setupGameStart
- Purpose: Sets up the game start with the selected map.
- Calls: TheWritableGlobalData->m_pendingFile, TheShell->reverseAnimatewindow()

### doGameStart
- Purpose: Initiates the game start process with selected difficulty and map.
- Calls: TheGameLogic->isInGame(), TheGameLogic->clearGameData(), TheMessageStream->appendMessage(), InitRandom()

### shutdownComplete
- Purpose: Completes the shutdown process for the map selection menu.
- Calls: layout->hide(), TheShell->shutdownComplete()

### SetDifficultyRadioButton
- Purpose: Sets the difficulty radio button based on the current script engine difficulty.
- Calls: TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), GadgetRadioSetSelection()

### MapSelectMenuInit
- Purpose: Initializes the map selection menu, including map list population and UI setup.
- Calls: TheShell->showShellMap(), TheMapCache->updateCache(), populateMapListbox(), TheShell->registerWithAnimateManager(), SetDifficultyRadioButton(), TheWindowManager->winSetFocus(), GadgetRadioSetSelection()

### MapSelectMenuShutdown
- Purpose: Shuts down the map selection menu.
- Calls: TheShell->reverseAnimatewindow(), shutdownComplete()

### MapSelectMenuUpdate
- Purpose: Updates the map selection menu state.
- Calls: TheShell->isAnimFinished(), doGameStart(), shutdownComplete()

### MapSelectMenuInput
- Purpose: Handles input events for the map selection menu.
- Calls: TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), TheWindowManager->winSendSystemMsg()

### MapSelectMenuSystem
- Purpose: Handles system messages for the map selection menu.
- Calls: TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), GadgetListBoxGetSelected(), GadgetListBoxGetItemData(), TheCampaignManager->setCampaign(), setupGameStart(), GadgetListBoxSetSelected(), TheWindowManager->winSendSystemMsg()

## Globals
- **radioButtonSystemMapsID (NameKeyType)**: ID for the system maps radio button.
- **radioButtonUserMapsID (NameKeyType)**:
