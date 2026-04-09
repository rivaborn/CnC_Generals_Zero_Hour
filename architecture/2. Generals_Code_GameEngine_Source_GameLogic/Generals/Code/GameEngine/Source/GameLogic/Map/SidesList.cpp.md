# Generals/Code/GameEngine/Source/GameLogic/Map/SidesList.cpp

## Purpose
This file contains the implementation for managing sides (players, AI, neutral entities) in a Command & Conquer Generals scenario, including parsing and writing side data chunks.

## Responsibilities
- Manage player and team information.
- Parse and write side data chunks.
- Handle build lists for non-player sides.
- Validate and ensure consistency of team and player relationships.

## Key Types
- **SidesInfo (Class)**: Manages information about a single side, including build lists and scripts.
- **BuildListInfo (Class)**: Represents an entry in the build list for a side.
- **TeamsInfoRec (Class)**: Manages a collection of team information.
- **TeamsInfo (Struct)**: Holds data for a single team.

## Key Functions
### ParseSidesDataChunk
- Purpose: Parses a sides data chunk from a file.
- Calls:
  - `file.readInt()`
  - `file.readDict()`
  - `file.readAsciiString()`
  - `file.readReal()`
  - `file.readByte()`

### WriteSidesDataChunk
- Purpose: Writes side data to a chunk writer.
- Calls:
  - `chunkWriter.openDataChunk()`
  - `chunkWriter.writeInt()`
  - `chunkWriter.writeDict()`
  - `chunkWriter.writeAsciiString()`
  - `chunkWriter.writeReal()`
  - `chunkWriter.writeByte()`

## Globals
- **K_SIDES_DATA_VERSION_1 (Int)**: Version constant for sides data.
- **K_SIDES_DATA_VERSION_2 (Int)**: Version constant for sides data including team list.
- **K_SIDES_DATA_VERSION_3 (Int)**: Version constant for sides data with additional build list info.
- **TheSidesList (SidesList*)**: Singleton instance of the SidesList class.

## Dependencies
- Includes:
  - "Common/DataChunk.h"
  - "Common/GameState.h"
  - "Common/PlayerTemplate.h"
  - "Common/WellKnownKeys.h"
  - "Common/Xfer.h"
  - "GameLogic/AI.h"
  - "GameLogic/Scripts.h"
  - "GameLogic/SidesList.h"
