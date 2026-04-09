# GeneralsMD/Code/GameEngine/Source/GameLogic/Map/SidesList.cpp

## Purpose
Manages player, AI, and team data in a scenario, including build lists and scripting.

## Responsibilities
- Serializes/deserializes side and team data
- Manages build lists for non-player sides
- Validates side/team relationships
- Handles script lists for sides

## Key Types
- **SidesInfo (Class)**: Stores side-specific data (build lists, scripts)
- **SidesList (Class)**: Singleton managing all sides and teams
- **BuildListInfo (Class)**: Represents a buildable structure with properties
- **TeamsInfoRec (Class)**: Manages team data collection

## Key Functions
### ParseSidesDataChunk
- Purpose: Reads side/team data from a chunk file
- Calls: `file.readInt()`, `file.readDict()`, `addSide()`, `addTeam()`, `ScriptList::ParseScriptsDataChunk`

### WriteSidesDataChunk
- Purpose: Writes side/team data to a chunk file
- Calls: `chunkWriter.writeInt()`, `chunkWriter.writeDict()`, `ScriptList::WriteScriptsDataChunk`

### validateSides
- Purpose: Ensures side/team relationships are valid
- Calls: `findSideInfo()`, `findTeamInfo()`, `addTeam()`

## Globals
- **K_SIDES_DATA_VERSION_1 (Int)**: Version constant for data format
- **K_SIDES_DATA_VERSION_2 (Int)**: Version constant for data format
- **K_SIDES_DATA_VERSION_3 (Int)**: Version constant for data format
- **TheSidesList (SidesList*)**: Singleton instance of SidesList

## Dependencies
- `DataChunk.h`, `GameState.h`, `PlayerTemplate.h`, `WellKnownKeys.h`, `Xfer.h`
- `AI.h`, `Scripts.h`, `SidesList.h`
