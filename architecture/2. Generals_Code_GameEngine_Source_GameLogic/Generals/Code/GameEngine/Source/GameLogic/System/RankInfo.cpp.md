# Generals/Code/GameEngine/Source/GameLogic/System/RankInfo.cpp

## Purpose
This file manages rank information for players in the game, including initialization, resetting, and parsing rank definitions from INI files.

## Responsibilities
- Initialize and reset rank information.
- Parse rank definitions from INI files.
- Retrieve rank information based on level.

## Key Types
- RankInfoStore (Class): Manages a collection of rank information.
- RankInfo (Class): Represents individual rank details such as name, skill points needed, sciences granted, and science purchase points.

## Key Functions
### init
- Purpose: Initializes the rank info store by clearing existing rank information.
- Calls: `m_rankInfos.clear()`

### reset
- Purpose: Resets the rank info store by deleting overrides for each rank.
- Calls: `deleteOverrides()`, `erase()`

### getRankLevelCount
- Purpose: Returns the number of ranks.
- Calls: None

### getRankInfo
- Purpose: Retrieves rank information based on level.
- Calls: `getFinalOverride()`

### friend_parseRankDefinition
- Purpose: Parses rank definitions from an INI file and updates or adds new rank information.
- Calls: `scanInt()`, `parseAndTranslateLabel()`, `parseInt()`, `parseScienceVector()`, `parseUnsignedInt()`, `newInstance()`, `initFromINI()`

### parseRankDefinition
- Purpose: Wrapper function to call `friend_parseRankDefinition`.
- Calls: `friend_parseRankDefinition()`

## Globals
- TheRankInfoStore (RankInfoStore*): Global instance of the rank info store.

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "Common/Player.h"
  - "GameLogic/RankInfo.h"
