# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupPlayerInfo.cpp

## Purpose
Handles the player info popup overlay in the GameSpy interface, displaying player statistics, battle honors, and allowing account management.

## Responsibilities
- Manages the player info overlay UI (init/shutdown/update/input)
- Displays player stats (wins/losses, rank, disconnects)
- Populates battle honors and tooltips
- Handles account management (locale, font preferences, account deletion)
- Processes GameSpy persistent storage responses

## Key Types
- `RankPoints` (Class): Stores rank point values and multipliers
- `TheRankPointValues` (Global): Singleton for rank point configuration
- `PSPlayerStats` (Struct): Player statistics from GameSpy

## Key Functions
### `lookupRankImage`
- Purpose: Finds the appropriate rank image based on player side and rank
- Calls: `TheMappedImageCollection->findImageByName`

### `CalculateRank`
- Purpose: Computes player rank points from their statistics
- Calls: `TheGameSpyConfig->getPointsForRank`

### `PopulatePlayerInfoWindows`
- Purpose: Updates the player info display with current statistics
- Calls: `GadgetListBoxAddEntryText`, `GameSpyPSMessageQueue->trackPlayerStats`

### `GameSpyPlayerInfoOverlaySystem`
- Purpose: Handles UI events for the player info overlay
- Calls: `GameSpyCloseOverlay`, `GameSpyOpenOverlay`, `MessageBoxYesNo`

## Globals
- `parentID`/`listboxInfoID`/`buttonCloseID` (NameKeyType): UI element identifiers
- `parent`/`listboxInfo`/`buttonClose` (GameWindow*): Pointers to UI elements
- `isOverlayActive` (Bool): Tracks overlay state
- `TheRankPointValues` (RankPoints*): Global rank configuration
- `rankNames` (const char*): Array of rank name strings

## Dependencies
- GameSpy networking modules (`PeerThread`, `PersistentStorageThread`)
- UI components (`WindowLayout`, `GadgetListBox`, `MessageBox`)
- Game text and localization (`GameText`)
- Player statistics (`BattleHonors`, `RankPointValue`)
