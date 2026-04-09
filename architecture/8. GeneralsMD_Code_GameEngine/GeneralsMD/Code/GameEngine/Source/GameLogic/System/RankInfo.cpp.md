# GeneralsMD/Code/GameEngine/Source/GameLogic/System/RankInfo.cpp

## Purpose
Manages player rank information and parsing rank definitions from INI files.

## Responsibilities
- Stores and manages `RankInfo` objects in a collection
- Parses rank definitions from INI files
- Handles rank overrides and resets
- Provides access to rank information by level

## Key Types
- `RankInfo` (Class): Stores rank-specific data (name, skill points, sciences)
- `RankInfoStore` (Class): Manages collection of `RankInfo` objects
- `TheRankInfoStore` (Global): Singleton instance of `RankInfoStore`

## Key Functions
### `RankInfoStore::init()`
- Purpose: Initializes the rank info store
- Calls: `m_rankInfos.clear()`

### `RankInfoStore::reset()`
- Purpose: Resets rank overrides without clearing base ranks
- Calls: `deleteOverrides()`, `erase()`

### `RankInfoStore::getRankInfo(Int level)`
- Purpose: Retrieves rank info for a specific level (1-based)
- Calls: `getFinalOverride()`

### `RankInfoStore::friend_parseRankDefinition(INI* ini)`
- Purpose: Parses rank definitions from INI files
- Calls: `newInstance()`, `setNextOverride()`, `markAsOverride()`, `initFromINI()`

## Globals
- `TheRankInfoStore` (RankInfoStore*): Global singleton instance of the rank info store

## Dependencies
- `PreRTS.h`, `Common/INI.h`, `Common/Player.h`, `GameLogic/RankInfo.h`
- `INI` class methods for parsing
- `Overridable` base class functionality
