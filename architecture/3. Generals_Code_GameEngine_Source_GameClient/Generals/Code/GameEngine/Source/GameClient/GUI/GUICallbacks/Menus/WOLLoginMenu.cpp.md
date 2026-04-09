# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLoginMenu.cpp

## Purpose
Handles the Westwood Online (WOL) login menu UI, including account creation, login, and Terms of Service (TOS) display.

## Responsibilities
- Manages GameSpy login preferences (storing/loading credentials)
- Handles login attempts and account creation
- Displays TOS in either a web browser or text file
- Validates user input (nickname, age)
- Manages UI state and transitions

## Key Types
- **GameSpyLoginPreferences (Class)**: Manages stored login credentials and preferences
- **obfuscate (Function)**: Obfuscates passwords for storage
- **startPings (Function)**: Initiates server ping requests
- **shutdownComplete (Function)**: Cleans up resources when menu closes
- **EnableLoginControls (Function)**: Enables/disables login UI controls
- **WOLLoginMenuInit (Function)**: Initializes the login menu UI
- **WOLLoginMenuShutdown (Function)**: Shuts down the login menu
- **checkLogin (Function)**: Validates login credentials
- **WOLLoginMenuUpdate (Function)**: Handles periodic updates
- **WOLLoginMenuInput (Function)**: Processes user input
- **isNickOkay (Function)**: Validates nickname format
- **isAgeOkay (Function)**: Validates user age
- **WOLLoginMenuSystem (Function)**: Main UI event handler

## Key Functions
### obfuscate
- Purpose: Obfuscates strings for secure storage
- Calls: None (standalone utility)

### startPings
- Purpose: Initiates ping requests to GameSpy servers
- Calls: ThePinger->addRequest()

### shutdownComplete
- Purpose: Cleans up resources when menu closes
- Calls: TheShell->shutdownComplete(), loginPref->write()

### EnableLoginControls
- Purpose: Enables/disables login UI controls
- Calls: buttonLogin->winEnable(), etc.

### WOLLoginMenuInit
- Purpose: Initializes the login menu UI
- Calls: GadgetComboBoxAddEntry(), etc.

### checkLogin
- Purpose: Validates login credentials
- Calls: TheGameSpyBuddyMessageQueue->addRequest()

### WOLLoginMenuUpdate
- Purpose: Handles periodic updates (login timeout, etc.)
- Calls: timeGetTime(), etc.

### WOLLoginMenuInput
- Purpose: Processes user input events
- Calls: GadgetTextEntryGetText(), etc.

### isNickOkay
- Purpose: Validates nickname format
- Calls: None (standalone validation)

### isAgeOkay
- Purpose: Validates user age
- Calls: None (standalone validation)

### WOLLoginMenuSystem
- Purpose: Main UI event handler for login menu
- Calls: All other functions in this file

## Globals
- **webBrowserActive (Bool)**: Tracks if web browser is active for TOS
- **useWebBrowserForTOS (Bool)**: Preference for using web browser for TOS
- **isShuttingDown (Bool)**: Tracks shutdown state
- **buttonPushed (Bool)**: Tracks button press state
- **nextScreen (char*)**: Stores next screen to display
- **loginTimeoutInMS (UnsignedInt)**: Login timeout in milliseconds
- **loginAttemptTime (UnsignedInt)**: Timestamp of last login attempt
- **PREF_FILENAME (const char*)**: Filename for login preferences
- **loginPref (GameSpyLoginPreferences*)**: Global preferences instance
- **parentWOLLoginID (NameKeyType)**: Window ID for login menu
- **buttonBackID (
