# GeneralsMD/Code/GameEngine/Include/GameLogic/RankInfo.h

## Purpose
Defines data structures and interfaces for managing player rank information in the game.

## Responsibilities
- Declares `RankInfo` class to store rank-specific data (name, skill points, science grants)
- Provides `RankInfoStore` singleton for rank management (initialization, retrieval)
- Defines parsing interface for rank definitions from INI files
- Manages rank progression logic via skill points and science grants

## Key Types
- `RankInfo` (Class): Stores rank name, required skill points, and science grants
- `RankInfoStore` (Class): Singleton managing rank data and progression
- `RankInfoVec` (Class): Typedef for vector of `RankInfo*` (internal storage)
- `RankInfoMagicEnum` (Enum): Not inferable (likely memory pool glue)
- `RankInfo_GLUE_NOT_IMPLEMENTED` (Enum): Not inferable (likely memory pool glue)

## Key Functions
### `RankInfoStore::init`
- Purpose: Initializes the rank system
- Calls: Not inferable (likely calls `friend_parseRankDefinition`)

### `RankInfoStore::getRankInfo`
- Purpose: Retrieves rank info by level (1-based)
- Calls: None visible

### `RankInfoStore::friend_parseRankDefinition`
- Purpose: Parses rank definitions from INI files
- Calls: None visible

## Globals
- `TheRankInfoStore` (RankInfoStore*): Global singleton instance of rank store

## Dependencies
- `Common/Science.h` (for `ScienceVec`)
- `Common/UnicodeString.h` (for rank names)
- `Common/STLTypedefs.h` (for STL containers)
- `Player` (forward-declared, likely for rank assignment)
- `INI` (for
