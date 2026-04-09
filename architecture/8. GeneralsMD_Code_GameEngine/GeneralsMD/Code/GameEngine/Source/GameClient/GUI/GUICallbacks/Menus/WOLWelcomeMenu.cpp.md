# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLWelcomeMenu.cpp

## Purpose
Handles the Westwood Online (WOL) welcome menu UI, including player stats, server info, and navigation to other menus.

## Responsibilities
- Manages WOL welcome menu initialization, updates, and shutdown
- Displays player stats (ladder/highscore) and server MOTD
- Handles button inputs for menu navigation
- Processes GameSpy peer responses and buddy messages
- Manages firewall detection and behavior

## Key Types
- `WOLWelcomeMenuInit()` (Function): Initializes the welcome menu UI
- `WOLWelcomeMenuUpdate()` (Function): Updates menu state and processes messages
- `WOLWelcomeMenuInput()` (Function): Handles keyboard input
- `WOLWelcomeMenuSystem()` (Function): Handles window system messages
- `GameWindow` (Type): UI window reference

## Key Functions
### `updateNumPlayersOnline()`
- Purpose: Updates the player count display and MOTD listbox
- Calls: `GadgetListBoxReset`, `GadgetListBoxAddEntryText`

### `HandleOverallStats()`
- Purpose: Parses win/loss statistics from GameSpy
- Calls: `strstr`, `FindNextNumber`, `s_winStats.insert`

### `WOLWelcomeMenuInit()`
- Purpose: Initializes the welcome menu UI and loads data
- Calls: `enableControls`, `updateNumPlayersOnline`, `updateOverallStats`

### `WOLWelcomeMenuUpdate()`
- Purpose: Updates menu state and processes GameSpy messages
- Calls: `HandleBuddyResponses`, `HandlePersistentStorageResponses`, `enableControls`

### `WOLWelcomeMenuSystem()`
- Purpose: Handles window system messages (button clicks, etc.)
- Calls: `TearDownGameSpy`, `TheShell->pop`, `GameSpyOpenOverlay`

## Globals
- `isShuttingDown` (Bool): Tracks shutdown state
- `buttonPushed` (Bool): Tracks button press state
- `nextScreen` (char*): Next screen to display
- `gServerName` (UnicodeString): Current server name
- `s_winStats` (map): Win/loss statistics by faction
- `lastNumPlayersOnline` (Int): Last player count received

## Dependencies
- GameSpy peer/buddy/persistent storage APIs
- Window management (`TheWindowManager`)
- Game text (`TheGameText`)
- Shell (`TheShell`)
- Transition handler (`TheTransitionHandler`)
- Firewall helper (`TheFirewallHelper`)
- Player template store (`ThePlayerTemplateStore`)
