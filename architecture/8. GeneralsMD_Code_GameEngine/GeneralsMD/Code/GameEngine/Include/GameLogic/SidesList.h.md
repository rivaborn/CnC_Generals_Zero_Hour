# GeneralsMD/Code/GameEngine/Include/GameLogic/SidesList.h

## Purpose
Header file defining classes for managing game sides (players), teams, and build lists in Command & Conquer Generals.

## Responsibilities
- Defines data structures for player sides and teams
- Manages build lists for structures
- Provides serialization/deserialization for game data
- Handles player/team relationships and validation

## Key Types
- **SidesInfo (Class)**: Stores build list and player-specific data
- **TeamsInfo (Class)**: Contains team-specific dictionary data
- **TeamsInfoRec (Class)**: Manages collection of team info objects
- **SidesList (Class)**: Singleton managing all sides and teams
- **BuildListInfo (Class)**: Represents individual buildable items in build lists
- **MAX_TEAM_DEPTH (Enum)**: Constant for maximum team nesting depth

## Key Functions
### ParseSidesDataChunk
- Purpose: Parses side data from input stream
- Calls: DataChunkInput operations

### WriteSidesDataChunk
- Purpose: Writes side data to output stream
- Calls: DataChunkOutput operations

### isBuildable
- Purpose: Checks if a build list item can be built again
- Calls: getNumRebuilds

## Globals
- **TheSidesList (SidesList*)**: Singleton instance of the sides list manager

## Dependencies
- Common/Dict.h, Common/Errors.h, Common/GameType.h
- Common/Snapshot.h, Common/GameMemory.h, Common/STLTypedefs.h
- DataChunkInput, DataChunkInfo, DataChunkOutput classes
- MemoryPoolObject, Snapshot interfaces
