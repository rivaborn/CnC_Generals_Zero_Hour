# GeneralsMD/Code/GameEngine/Source/Common/System/SaveGame/GameState.cpp

## Purpose
Manages game state serialization/deserialization for save/load functionality in Command & Conquer Generals.

## Responsibilities
- Handles save game file I/O operations
- Manages snapshot blocks for game state components
- Provides date/time formatting utilities
- Maintains available save game list
- Coordinates post-load processing

## Key Types
- `GameState` (Class): Main singleton managing save/load operations
- `SaveGameInfo` (Struct): Contains metadata about saved games
- `SaveDate` (Struct): Represents date/time information
- `SnapshotBlock` (Struct): Links block names to snapshot objects

## Key Functions
### `xferSaveData`
- Purpose: Serializes/deserializes game state data
- Calls: `xfer->xferAsciiString`, `xfer->beginBlock`, `xfer->endBlock`, `findBlockInfoByToken`

### `addPostProcessSnapshot`
- Purpose: Registers snapshots for post-load processing
- Calls: None (validation only)

### `gameStatePostProcessLoad`
- Purpose: Executes post-load processing for registered snapshots
- Calls: `snapshot->loadPostProcess`, `ThePartitionManager->update`

### `getUnicodeDateBuffer`
- Purpose: Formats date string for display
- Calls: `GetDateFormat`/`GetDateFormatW`

### `getUnicodeTimeBuffer`
- Purpose: Formats time string for display
- Calls: `GetTimeFormat`/`GetTimeFormatW`

## Globals
- `TheGameState` (GameState*): Singleton instance
- `SAVE_FILE_EOF` (Char*): End-of-file marker
- `SAVE_GAME_EXTENSION` (Char*): File extension
- `ZERO_NAME_ONLY` (Char*): Default filename
- `MAX_SAVE_FILE_NUMBER` (Int): Max save number
- `PORTABLE_SAVE` (Bool): Portable save flag
- `PORTABLE_MAPS` (Bool): Portable maps flag
- `PORTABLE_USER_MAPS` (Bool): Portable user maps flag

## Dependencies
- `Xfer.h` for serialization
- `File.h`/`FileSystem.h` for file I/O
- `GameEngine.h` for core systems
- `CampaignManager.h` for campaign data
- Windows API for date/time formatting
