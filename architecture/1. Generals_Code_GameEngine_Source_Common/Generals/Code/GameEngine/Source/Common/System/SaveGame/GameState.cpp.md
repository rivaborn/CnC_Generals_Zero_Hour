# Generals/Code/GameEngine/Source/Common/System/SaveGame/GameState.cpp

## Purpose
Handles game state management, including saving and loading games, managing available save files, and processing post-load operations.

## Responsibilities
- Manages the game state singleton.
- Handles saving and loading of game data using Xfer objects.
- Maintains a list of snapshot blocks for different types of game data.
- Provides utility functions for date and time formatting.
- Iterates through directories to find save files.

## Key Types
- `SaveGameInfo`: Stores information about a saved game, such as date, mission number, and file type.
- `SaveDate`: Represents a date with methods to compare dates.
- `SnapshotBlock`: Contains information about a snapshot block for saving/loading.
- `GameState`: Manages the overall game state, including available games and post-load processing.

## Key Functions
### getUnicodeDateBuffer
- Purpose: Formats the current system time into a Unicode string representing the date.
- Calls: `GetVersionEx`, `GetDateFormatW`

### getUnicodeTimeBuffer
- Purpose: Formats the current system time into a Unicode string representing the time.
- Calls: `GetVersionEx`, `GetTimeFormatW`

### findHighFileNumber
- Purpose: Finds the highest file number in a directory for save files.
- Calls: `FindFirstFile`, `FindNextFile`

### addGameToAvailableList
- Purpose: Adds a game to the list of available games.
- Calls: None

### GameState::init
- Purpose: Initializes the game state subsystem by adding snapshot blocks for saving/loading.
- Calls: `addSnapshotBlock`

### GameState::xferSaveData
- Purpose: Saves or loads game data using Xfer objects, handling different snapshot types.
- Calls: `xferAsciiString`, `beginBlock`, `xferSnapshot`, `endBlock`

## Globals
- `TheGameState (GameState*)`: The singleton instance of the game state.
- `SAVE_FILE_EOF (const Char*)`: End-of-file token for save files.
- `SAVE_GAME_EXTENSION (const Char*)`: File extension for save files.
- `ZERO_NAME_ONLY (const Char*)`: Constant string "00000000".
- `MAX_SAVE_FILE_NUMBER (Int)`: Maximum number for save file numbering.

## Dependencies
- Key includes: `Common/File.h`, `Common/FileSystem.h`, `Common/GameEngine.h`, `Common/GameState.h`, `Common/XferLoad.h`, `Common/XferSave.h`, `GameClient/CampaignManager.h`, `GameLogic/GameLogic.h`.
- External symbols: `GetVersionEx`, `GetDateFormatW`, `GetTimeFormatW`, `FindFirstFile`, `FindNextFile`
