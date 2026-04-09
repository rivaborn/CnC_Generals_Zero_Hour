# GeneralsMD/Code/GameEngine/Include/Common/GameState.h

## Purpose
Header defining the game state management system for saving, loading, and validating game states in Command & Conquer Generals.

## Responsibilities
- Defines data structures for save game metadata (dates, descriptions, map info)
- Declares the `GameState` singleton class for save/load operations
- Provides enums for save types, error codes, and snapshot types
- Manages snapshot blocks for modular save/load functionality

## Key Types
- **GameState (Class)**: Singleton managing game save/load operations and snapshot handling
- **SaveGameInfo (Class)**: Contains metadata about a saved game (map, date, description, etc.)
- **SaveDate (Struct)**: Stores date/time information for save files
- **SaveCode (Enum)**: Error codes for save/load operations
- **SnapshotType (Enum)**: Types of snapshots (SAVELOAD, DEEPCRC, etc.)

## Key Functions
### `saveGame`
- Purpose: Saves the current game state to a file
- Calls: `findNextSaveFilename`, `xferSaveData`

### `loadGame`
- Purpose: Loads a saved game from a file
- Calls: `xferSaveData`, `gameStatePostProcessLoad`

### `populateSaveGameListbox`
- Purpose: Populates a UI listbox with available save games
- Calls: `iterateSaveFiles`

## Globals
- **TheGameState (GameState*)**: Global instance of the GameState singleton

## Dependencies
- `Common/STLTypedefs.h`, `Common/Snapshot.h`, `Common/SubsystemInterface.h`, `Common/UnicodeString.h`
- `GameNetwork/NetworkDefs.h`
- Forward references: `GameWindow`, `WindowLayout`
