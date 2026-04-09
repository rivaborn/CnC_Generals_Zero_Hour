# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLWelcomeMenu.cpp

## Purpose
Handles the Welcome menu UI for the Westwood Online (WOL) lobby system in Command & Conquer Generals.

## Responsibilities
- Manages UI elements for the WOL welcome screen
- Handles player stats and server info display
- Processes GameSpy peer messages and buddy responses
- Controls navigation between WOL menus
- Manages firewall detection and behavior

## Key Types
- `OverallStats` (Struct): Tracks wins/losses statistics per faction
- `GameWindow` pointers: UI element references (buttons, text fields)
- `NameKeyType`: Window ID identifiers

## Key Functions
### `updateServerDisplay`
- Purpose: Updates the server name display
- Calls: `GadgetStaticTextSetText`

### `enableControls`
- Purpose: Enables/disables menu buttons based on GameSpy state
- Calls: `winEnable`

### `HandleNumPlayersOnline`
- Purpose: Updates player count and MOTD display
- Calls: `GadgetStaticTextSetText`, `GadgetListBoxAddEntryText`

### `HandleOverallStats`
- Purpose: Processes and displays faction statistics
- Calls: `calcPercent`, `GadgetStaticTextSetText`

### `WOLWelcomeMenuInit`
- Purpose: Initializes the welcome menu UI
- Calls: `TheWindowManager->winGetWindowFromId`, `enableControls`, `updateNumPlayersOnline`

### `WOLWelcomeMenuSystem`
- Purpose: Handles UI system messages and button clicks
- Calls: `PeerRequest`, `BuddyRequest`, `GameSpyOpenOverlay`, `TheShell->pop`

## Globals
- `isShuttingDown` (Bool): Tracks shutdown state
- `buttonPushed` (Bool): Tracks button press state
- `nextScreen` (char*): Stores next menu to display
- `gServerName` (UnicodeString): Current server name
- `lastNumPlayersOnline` (Int): Last known player count
- `s_statsUSA/China/GLA` (OverallStats): Faction statistics

## Dependencies
- GameSpy peer/buddy chat APIs
- Window management and UI gadget systems
- Game text and localization
- Firewall helper utilities
- Shell and transition handlers
