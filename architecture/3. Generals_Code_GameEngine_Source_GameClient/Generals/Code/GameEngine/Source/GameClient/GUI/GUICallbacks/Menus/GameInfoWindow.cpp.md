# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/GameInfoWindow.cpp

## Purpose
Manages the LAN game info window UI, including creation, destruction, refresh, and hiding.

## Responsibilities
- Create and destroy the game info window layout
- Refresh window content with game info (name, map, players)
- Handle window initialization and system messages
- Manage player list display with colors and icons

## Key Types
- `GameWindow` (Class): Base window class for UI elements
- `WindowLayout` (Class): Layout manager for UI windows
- `GameInfo` (Class): Contains game session information
- `LANGameInfo` (Class): LAN-specific game info
- `GameSlot` (Class): Represents a player slot in a game
- `PlayerTemplate` (Enum): Defines player factions/sides

## Key Functions
### CreateLANGameInfoWindow
- Purpose: Creates and positions the game info window
- Calls: `winCreateLayout`, `runInit`, `bringForward`, `hide`, `winGetScreenPosition`, `winSetPosition`, `winGetSize`, `winSetSize`

### DestroyGameInfoWindow
- Purpose: Destroys the game info window layout
- Calls: `destroyWindows`, `deleteInstance`

### RefreshGameInfoWindow
- Purpose: Updates window content with current game info
- Calls: `winHide`, `winBringToTop`, `GadgetStaticTextSetText`, `GadgetListBoxReset`, `GadgetListBoxAddEntryText`, `GadgetListBoxAddEntryImage`, `fetch`, `getNthPlayerTemplate`, `getSideIconImage`

### HideGameInfoWindow
- Purpose: Shows or hides the game info window
- Calls: `winHide`

### GameInfoWindowInit
- Purpose: Initializes window components and IDs
- Calls: `nameToKey`, `winGetWindowFromId`, `GadgetStaticTextSetText`, `GadgetListBoxReset`

### GameInfoWindowSystem
- Purpose: Handles system messages for the game info window
- Calls: None (handles messages internally)

## Globals
- `parent` (GameWindow*): Main window container
- `staticTextGameName` (GameWindow*): Game name display
- `staticTextMapName` (GameWindow*): Map name display
- `listBoxPlayers` (GameWindow*): Player list display
- `winCrates` (GameWindow*): Crates option display
- `winSuperWeapons` (GameWindow*): Super weapons option display
- `winFreeForAll` (GameWindow*): Free-for-all option display
- `parentID` (NameKeyType): ID for parent window
- `staticTextGameNameID` (NameKeyType
