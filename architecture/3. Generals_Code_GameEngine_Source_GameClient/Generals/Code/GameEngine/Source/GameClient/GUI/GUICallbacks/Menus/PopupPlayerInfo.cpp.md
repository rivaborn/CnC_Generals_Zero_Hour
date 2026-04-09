# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupPlayerInfo.cpp

## Purpose
Handles the player info popup overlay in the GameSpy lobby, displaying player statistics, battle honors, and allowing account management.

## Responsibilities
- Manages the player info overlay UI (init, update, shutdown, input)
- Displays player stats (rank, wins, losses, disconnects)
- Handles battle honors tooltip display
- Manages account settings (locale, font preferences, account deletion)
- Processes GameSpy persistent storage responses for player data

## Key Types
- `RankPoints` (Class): Stores rank point values and multipliers for player ranking calculation
- `TheRankPointValues` (Global): Singleton instance of RankPoints for global access
- `PSPlayerStats` (Struct): Player statistics structure from GameSpy

## Key Functions
### `lookupRankImage`
- Purpose: Finds and returns the rank image for a given side and rank
- Calls: `TheMappedImageCollection->findImageByName`

### `CalculateRank`
- Purpose: Computes a player's rank points based on their statistics
- Calls: `TheGameSpyConfig->getPointsForRank`, `TheRankPointValues->getPointsForRank`

### `PopulatePlayerInfoWindows`
- Purpose: Fills the player info listbox with statistics and battle honors
- Calls: `GadgetListBoxAddEntryText`, `populateBattleHonors`, `GetAdditionalDisconnectsFromUserFile`

### `HandlePersistentStorageResponses`
- Purpose: Processes GameSpy persistent storage responses to update player info
- Calls: `TheGameSpyPSMessageQueue->trackPlayerStats`, `UpdateLocalPlayerStats`, `PopulatePlayerInfoWindows`

### `GameSpyPlayerInfoOverlaySystem`
- Purpose: Handles UI events for the player info overlay
- Calls: `GameSpyCloseOverlay`, `GameSpyOpenOverlay`, `MessageBoxYesNo`

## Globals
- `parentID` (NameKeyType): ID for the parent window
- `listboxInfoID` (NameKeyType): ID for the info listbox
- `buttonCloseID` (NameKeyType): ID for the close button
- `buttonBuddiesID` (NameKeyType): ID for the buddies button
- `buttonSetLocaleID` (NameKeyType): ID for the locale button
- `buttonDeleteAccountID` (NameKeyType): ID for the delete account button
- `checkBoxAsianFontID` (NameKeyType): ID for the Asian font checkbox
- `checkBoxNonAsianFontID` (NameKeyType): ID for the non-Asian font checkbox
- `parent` (GameWindow*): Pointer to the parent window
- `listboxInfo` (GameWindow*): Pointer to the info listbox
- `buttonClose` (GameWindow*): Pointer to the close button
- `buttonBuddies` (GameWindow*): Pointer to the buddies button
- `buttonSetLocale` (GameWindow*): Pointer to the locale button
- `buttonDeleteAccount` (GameWindow*): Pointer to the delete account button
- `checkBoxAsianFont` (GameWindow*): Pointer to the Asian font checkbox
- `checkBoxNonAsianFont` (GameWindow*): Pointer to the non-Asian font checkbox
- `isOverlayActive` (Bool): Tracks if the overlay is active
- `raiseMessageBox` (Bool): Flag to raise a message box
- `lookAtPlayerID` (Int): ID of the player to display info for
- `lookAtPlayerName` (std::string): Name of the player to display info for
- `rankNames` (const char*): Array of rank name strings
