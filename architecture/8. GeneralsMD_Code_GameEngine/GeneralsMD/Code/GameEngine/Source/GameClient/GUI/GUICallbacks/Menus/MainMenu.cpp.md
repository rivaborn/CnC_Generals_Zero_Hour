# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/MainMenu.cpp

## Purpose
Handles the main menu UI system for Command & Conquer Generals Zero Hour, including menu navigation, game initialization, and CD checks.

## Responsibilities
- Manages main menu window layout and transitions
- Handles user input for menu navigation and game start
- Coordinates CD checks before campaign start
- Manages game difficulty selection
- Handles resolution change dialogs

## Key Types
- DROPDOWN_NONE (Enum): No dropdown active
- DROPDOWN_SINGLE (Enum): Single player dropdown active
- DROPDOWN_MULTIPLAYER (Enum): Multiplayer dropdown active
- DROPDOWN_MAIN (Enum): Main menu dropdown active
- DROPDOWN_LOADREPLAY (Enum): Load replay dropdown active
- DROPDOWN_DIFFICULTY (Enum): Difficulty selection dropdown active
- SHOW_NONE (Enum): No faction shown
- SHOW_TRAINING (Enum): Training faction shown
- SHOW_USA (Enum): USA faction shown
- SHOW_GLA (Enum): GLA faction shown
- SHOW_CHINA (Enum): China faction shown
- SHOW_SKIRMISH (Enum): Skirmish mode shown

## Key Functions
### MainMenuSystem
- Purpose: Handles all main menu input events and navigation
- Calls: TheShell->push, TheTransitionHandler->setGroup, TheCampaignManager->setCampaign, checkCDBeforeCampaign

### MainMenuInit
- Purpose: Initializes the main menu UI and sets up all menu elements
- Calls: TheWindowManager->winCreateLayout, TheTransitionHandler->setGroup, TheCampaignManager->setCampaign

### MainMenuShutdown
- Purpose: Cleans up main menu resources
- Calls: TheWindowManager->winDestroyLayout, TheTransitionHandler->remove

### checkCDBeforeCampaign
- Purpose: Checks for CD presence before starting a campaign
- Calls: IsFirstCDPresent, ExMessageBoxOkCancel, prepareCampaignGame

### setupGameStart
- Purpose: Prepares to start a game with specified map and difficulty
- Calls: TheCampaignManager->setGameDifficulty, TheShell->push, TheTransitionHandler->reverse

## Globals
- raiseMessageBoxes (Bool): Controls whether message boxes are shown
- campaignSelected (Bool): Tracks if a campaign has been selected
- mainMenuID (NameKeyType): ID for main menu window
- skirmishID (NameKeyType): ID for skirmish menu window
- onlineID (NameKeyType): ID for online menu window
- networkID (NameKeyType): ID for network menu window
- optionsID (NameKeyType): ID for options menu window
- exitID (NameKeyType): ID for exit button
- motdID (NameKeyType): ID for MOTD window
- worldBuilderID (NameKeyType): ID for world builder button
- getUpdateID (NameKeyType): ID for update button
- parentMainMenu (GameWindow*): Pointer to main menu window
- buttonSinglePlayer (GameWindow*): Pointer to single player button
- buttonMultiPlayer (GameWindow*): Pointer to multiplayer button
- buttonSkirmish (GameWindow*): Pointer to skirmish button
- buttonOnline (GameWindow*): Pointer to online button
- buttonNetwork (GameWindow*): Pointer to network button
- buttonOptions (GameWindow*): Pointer to options button
- buttonExit (GameWindow*): Pointer to exit button
- buttonMOTD (GameWindow*): Pointer to MOTD button
- buttonWorldBuilder (GameWindow*): Pointer to world builder button
- mainMenuMovie (GameWindow*): Pointer
