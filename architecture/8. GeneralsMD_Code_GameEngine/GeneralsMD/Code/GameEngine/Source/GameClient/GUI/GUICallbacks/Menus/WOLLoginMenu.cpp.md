# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLoginMenu.cpp

## Purpose
Handles the Westwood Online (WOL) login menu system, including user authentication, account creation, and preferences management.

## Responsibilities
- Manages GameSpy login UI and workflow
- Handles account creation and login requests
- Stores/recalls login credentials via `GameSpyLoginPreferences`
- Validates user input (nickname, age, etc.)
- Coordinates with GameSpy networking threads

## Key Types
- **GameSpyLoginPreferences (Class)**: Manages stored login credentials and preferences
- **obfuscate (Function)**: Simple XOR-based string obfuscation utility
- **startPings (Function)**: Initiates server ping requests
- **shutdownComplete (Function)**: Cleanup handler for menu shutdown
- **EnableLoginControls (Function)**: Enables/disables login UI elements
- **WOLLoginMenuInit (Function)**: Initializes the login menu UI
- **WOLLoginMenuShutdown (Function)**: Cleans up login menu resources
- **checkLogin (Function)**: Validates login credentials
- **WOLLoginMenuUpdate (Function)**: Handles periodic menu updates
- **WOLLoginMenuInput (Function)**: Processes user input events
- **isNickOkay (Function)**: Validates nickname format
- **isAgeOkay (Function)**: Validates user age input
- **WOLLoginMenuSystem (Function)**: Main event handler for login menu

## Key Functions
### obfuscate
- Purpose: Simple XOR-based string obfuscation
- Calls: None

### startPings
- Purpose: Initiates server ping requests for latency measurement
- Calls: `TheGameSpyConfig->getPingServers()`, `TheGameSpyConfig->getPingTimeoutInMs()`, `TheGameSpyConfig->getNumPingRepetitions()`, `ThePinger->addRequest()`

### shutdownComplete
- Purpose: Handles cleanup when login menu shuts down
- Calls: `layout->hide()`, `TheShell->shutdownComplete()`, `loginPref->write()`, `delete loginPref`

### EnableLoginControls
- Purpose: Enables/disables login UI controls based on state
- Calls: `buttonLogin->winEnable()`, `buttonCreateAccount->winEnable()`, etc.

### WOLLoginMenuInit
- Purpose: Initializes the login menu UI and loads preferences
- Calls: `loginPref->load()`, various Gadget* initialization functions

### WOLLoginMenuShutdown
- Purpose: Cleans up login menu resources
- Calls: `loginPref->write()`, `delete loginPref`

### checkLogin
- Purpose: Validates login credentials against server
- Calls: `TheGameSpyBuddyMessageQueue->addRequest()`

### WOLLoginMenuUpdate
- Purpose: Handles periodic menu updates and login timeouts
- Calls: `timeGetTime()`, `TheGameSpyBuddyMessageQueue->getResponse()`

### WOLLoginMenuInput
- Purpose: Processes user input events for login menu
- Calls: Various Gadget* functions, `GSMessageBoxOk()`

### isNickOkay
- Purpose: Validates nickname format
- Calls: None

### isAgeOkay
- Purpose: Validates user age input
- Calls: None

### WOLLoginMenuSystem
- Purpose: Main event handler for login menu
- Calls: All other functions in this file

## Globals
- **webBrowserActive (Bool)**: Tracks if web browser is active for TOS
- **useWebBrowserForTOS (Bool)**: Whether to use web browser for TOS display
- **isShuttingDown (Bool)**: Tracks if
