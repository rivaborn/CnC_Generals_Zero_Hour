# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/LobbyUtils.cpp

## Purpose
Handles GameSpy lobby UI utilities, including game list management, sorting, and tooltips.

## Responsibilities
- Manages game list display and sorting
- Handles lobby UI tooltips
- Maintains buddy game tracking
- Refreshes game lists based on sorting criteria
- Provides access to game list UI elements

## Key Types
- COLUMN_NAME (Enum): Column index for game name
- COLUMN_MAP (Enum): Column index for map name
- COLUMN_LADDER (Enum): Column index for ladder info
- COLUMN_NUMPLAYERS (Enum): Column index for player count
- COLUMN_PASSWORD (Enum): Column index for password status
- COLUMN_OBSERVER (Enum): Column index for observer status
- COLUMN_USE_STATS (Enum): Column index for stats usage
- COLUMN_PING (Enum): Column index for ping status
- BuddyGameSet (Class): Set of buddy games
- GameSortStruct (Class): Functor for sorting games

## Key Functions
### showSortIcons
- Purpose: Updates sort icons based on current sort mode
- Calls: windowSortAlpha->winHide, windowSortPing->winHide, windowSortBuddies->winHide

### HandleSortButton
- Purpose: Handles sort button clicks and updates sort mode
- Calls: sortByBuddies, setSortMode

### gameTooltip
- Purpose: Generates tooltips for game list entries
- Calls: GadgetListBoxGetEntryBasedOnXY, TheMouse->setCursorTooltip

### insertGame
- Purpose: Adds a game to the listbox with appropriate formatting
- Calls: GadgetListBoxAddEntryText, GadgetListBoxAddEntryImage

### RefreshGameListBox
- Purpose: Refreshes the game list with current data
- Calls: populateBuddyGames, clearBuddyGames, insertGame

## Globals
- buttonSortAlphaID (NameKeyType): ID for alpha sort button
- buttonSortPingID (NameKeyType): ID for ping sort button
- buttonSortBuddiesID (NameKeyType): ID for buddy sort button
- theGameSortType (GameSortType): Current sort mode
- sortBuddies (Bool): Whether to sort by buddies
- parentID (NameKeyType): Parent window ID
- listboxLobbyGamesLargeID (NameKeyType): Large game list ID
- listboxLobbyGamesLarge (GameWindow*): Large game list window
- pingImages (Image*): Array of ping indicator images
- theBuddyGames (BuddyGameSet): Set of buddy games

## Dependencies
- GameClient headers (WindowManager, GadgetListBox, etc.)
- GameNetwork/GameSpy headers (Overlay, BuddyDefs, etc.)
- Common headers (GameEngine, MultiplayerSettings, etc.)
- External symbols: TheGameSpyInfo, TheWindowManager, TheMouse, etc.
