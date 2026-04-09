# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/LobbyUtils.cpp

## Purpose
Handles GameSpy lobby UI utilities, including game list management, sorting, and tooltips.

## Responsibilities
- Manages game list UI elements (list boxes, buttons)
- Implements game sorting by name, ping, and buddy status
- Displays tooltips for game information
- Refreshes game lists based on current data
- Handles window layout and visibility

## Key Types
- COLUMN_NAME (Enum): Column index for game name
- COLUMN_MAP (Enum): Column index for map name
- COLUMN_LADDER (Enum): Column index for ladder info
- COLUMN_NUMPLAYERS (Enum): Column index for player count
- COLUMN_PASSWORD (Enum): Column index for password status
- COLUMN_OBSERVER (Enum): Column index for observer status
- COLUMN_PING (Enum): Column index for ping value
- GameSortStruct (Class): Functor for sorting games
- BuddyGameSet (Class): Set of buddy games

## Key Functions
### showSortIcons
- Purpose: Updates sort indicator icons based on current sort mode
- Calls: winHide, winEnable

### setSortMode
- Purpose: Sets the game sort type and refreshes the list
- Calls: showSortIcons, RefreshGameListBoxes

### sortByBuddies
- Purpose: Toggles buddy sorting and refreshes the list
- Calls: showSortIcons, RefreshGameListBoxes

### HandleSortButton
- Purpose: Handles sort button clicks
- Calls: sortByBuddies, setSortMode

### gameTooltip
- Purpose: Generates tooltips for game list entries
- Calls: GadgetListBoxGetEntryBasedOnXY, TheMouse->setCursorTooltip

### insertGame
- Purpose: Adds a game to the list box with all its properties
- Calls: GadgetListBoxAddEntryText, GadgetListBoxAddEntryImage

### RefreshGameListBox
- Purpose: Refreshes the game list with current data
- Calls: GadgetListBoxReset, populateBuddyGames, clearBuddyGames

### RefreshGameListBoxes
- Purpose: Refreshes all game list UI elements
- Calls: RefreshGameListBox, RefreshGameInfoListBox

## Globals
- buttonSortAlphaID (NameKeyType): ID for alpha sort button
- buttonSortPingID (NameKeyType): ID for ping sort button
- buttonSortBuddiesID (NameKeyType): ID for buddy sort button
- theGameSortType (GameSortType): Current sort mode
- sortBuddies (Bool): Whether to sort by buddies
- parentID (NameKeyType): ID for parent window
- parentGameListLargeID (NameKeyType): ID for large game list parent
- listboxLobbyGamesSmallID (NameKeyType): ID for small game list
- listboxLobbyGamesLargeID (NameKeyType): ID for large game list
- parent (GameWindow*): Parent window pointer
- parentGameListLarge (GameWindow*): Large game list parent
- listboxLobbyGamesLarge (GameWindow*): Large game list
- pingImages (Image*): Array of ping indicator images
- isSmall (Bool): Whether using small UI mode
- theBuddyGames (BuddyGameSet*): Set of buddy games

## Dependencies
- GameClient headers (WindowLayout, Gadget, Image, etc.)
- GameNetwork/GameSpy headers (Overlay, BuddyDefs, LadderDefs, etc.)
- Common headers (GameEngine, MultiplayerSettings, etc.)
- External symbols: TheGameSpyInfo, TheWindowManager, TheMouse, etc.
