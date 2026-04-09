# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/MapSelectMenu.cpp

## Purpose
Handles the map selection menu UI, including map listing, difficulty settings, and game startup.

## Responsibilities
- Manages map list population and filtering (system/user maps, solo/multiplayer)
- Handles difficulty selection (easy/normal/hard)
- Initiates game startup with selected map and difficulty
- Manages menu navigation and animations

## Key Types
- None

## Key Functions
### setupGameStart
- Purpose: Prepares game startup with selected map
- Calls: TheWritableGlobalData->m_pendingFile, TheShell->reverseAnimatewindow()

### doGameStart
- Purpose: Initiates new game with selected difficulty and map
- Calls: TheGameLogic->clearGameData(), TheMessageStream->appendMessage(), InitRandom()

### SetDifficultyRadioButton
- Purpose: Updates UI to reflect current difficulty setting
- Calls: TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), GadgetRadioSetSelection()

### MapSelectMenuInit
- Purpose: Initializes the map selection menu UI
- Calls: TheShell->showShellMap(), TheMapCache->updateCache(), populateMapListbox(), TheShell->registerWithAnimateManager(), SetDifficultyRadioButton()

### MapSelectMenuSystem
- Purpose: Handles UI events for the map selection menu
- Calls: TheNameKeyGenerator->nameToKey(), TheWindowManager->winGetWindowFromId(), GadgetListBoxGetSelected(), GadgetListBoxGetItemData(), TheCampaignManager->setCampaign(), setupGameStart(), GadgetListBoxSetSelected()

## Globals
- radioButtonSystemMapsID (NameKeyType): ID for system maps radio button
- radioButtonUserMapsID (NameKeyType): ID for user maps radio button
- mapList (GameWindow*): Pointer to the map listbox window
- showSoloMaps (Bool): Flag for showing solo maps
- isShuttingDown (Bool): Flag for shutdown state
- startGame (Bool): Flag for game start state
- buttonPushed (Bool): Flag for button press state
- s_AIDiff (GameDifficulty): Current AI difficulty setting

## Dependencies
- PreRTS.h, GameEngine.h, MessageStream.h, RandomValue.h, UserPreferences.h, GameLogic.h, ScriptEngine.h, AnimateWindowManager.h, CampaignManager.h, WindowLayout.h, Gadget.h, Shell.h, GameWindowManager.h, GadgetListBox.h, GadgetRadioButton.h, MapUtil.h, Mouse.h
