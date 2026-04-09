# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/MainMenu.cpp

## Purpose
Handles the main menu UI and its callbacks in Command & Conquer Generals.

## Responsibilities
- Manages main menu window initialization and shutdown
- Handles button presses and menu transitions
- Controls campaign selection and game difficulty settings
- Manages CD checks for campaign start
- Handles resolution change dialogs

## Key Types
- DROPDOWN_* (Enum): dropdown menu types (NONE, SINGLE, MULTIPLAYER, etc.)
- SHOW_* (Enum): faction selection states (NONE, TRAINING, USA, GLA, CHINA, SKIRMISH)
- GameWindow pointers: UI elements (buttons, windows)

## Key Functions
### MainMenuInit
- Purpose: Initializes the main menu UI and its components
- Calls: TheWindowManager->winCreateLayout, TheTransitionHandler->setGroup, etc.

### MainMenuShutdown
- Purpose: Cleans up main menu resources
- Calls: TheWindowManager->winDestroyLayout, etc.

### MainMenuUpdate
- Purpose: Handles main menu updates and animations
- Calls: TheTransitionHandler->update, TheWindowManager->winUpdate, etc.

### MainMenuInput
- Purpose: Processes user input for the main menu
- Calls: TheWindowManager->winInput, etc.

### checkCDBeforeCampaign
- Purpose: Checks for CD presence before starting campaign
- Calls: ExMessageBoxOkCancel, prepareCampaignGame

### prepareCampaignGame
- Purpose: Sets up campaign game with selected difficulty
- Calls: TheCampaignManager->setGameDifficulty, setupGameStart

## Globals
- mainMenuID (NameKeyType): ID for main menu window
- buttonSinglePlayer (GameWindow*): pointer to single player button
- dropDownWindows (GameWindow*): array of dropdown menu windows
- campaignSelected (Bool): tracks if campaign is selected
- showSide (Int): current faction selection state
- isShuttingDown (Bool): tracks shutdown state

## Dependencies
- GameClient headers (WindowLayout, Gadget, Shell, etc.)
- GameNetwork headers (DownloadManager, GameSpyOverlay)
- Common headers (GameEngine, GameState, GlobalData)
- CDCheck.h for CD verification
