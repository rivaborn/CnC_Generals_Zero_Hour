# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/GameInfoWindow.cpp

## Purpose
Handles the creation, destruction, and management of the LAN game info window in the UI.

## Responsibilities
- Manages the game info window lifecycle (creation/destruction)
- Refreshes window content with game data (name, map, players)
- Initializes window layout and references to UI elements
- Handles window system messages

## Key Types
- None

## Key Functions
### CreateLANGameInfoWindow
- Purpose: Creates and positions the game info window based on a reference window.
- Calls: TheWindowManager->winCreateLayout, gameInfoWindowLayout->runInit, gameInfoWindowLayout->bringForward, gameInfoWindowLayout->hide

### DestroyGameInfoWindow
- Purpose: Destroys the game info window and cleans up resources.
- Calls: gameInfoWindowLayout->destroyWindows, gameInfoWindowLayout->deleteInstance

### RefreshGameInfoWindow
- Purpose: Updates the window with current game info (name, map, players).
- Calls: GadgetStaticTextSetText, TheMapCache->find, GadgetListBoxReset, GadgetListBoxAddEntryText, GadgetListBoxAddEntryImage

### HideGameInfoWindow
- Purpose: Shows or hides the game info window.
- Calls: parent->winHide

### GameInfoWindowInit
- Purpose: Initializes window layout and references to UI elements.
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetStaticTextSetText, GadgetListBoxReset

### GameInfoWindowSystem
- Purpose: Handles system messages for the game info window.
- Calls: None (handles messages internally)

## Globals
- parent (GameWindow*): Main window container
- staticTextGameName (GameWindow*): Game name display
- staticTextMapName (GameWindow*): Map name display
- listBoxPlayers (GameWindow*): Player list box
- winCrates (GameWindow*): Crates option window
- winSuperWeapons (GameWindow*): Super weapons option window
- winFreeForAll (GameWindow*): Free-for-all option window
- parentID (NameKeyType): ID for parent window
- staticTextGameNameID (NameKeyType): ID for game name text
- staticTextMapNameID (NameKeyType): ID for map name text
- listBoxPlayersID (NameKeyType): ID for player list box
- winCratesID (NameKeyType): ID for crates window
- winSuperWeaponsID (NameKeyType): ID for super weapons window
- winFreeForAllID (NameKeyType): ID for free-for-all window
- gameInfoWindowLayout (WindowLayout*): Window layout
