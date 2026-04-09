# GeneralsMD/Code/GameEngine/Source/Common/INI/INITerrainRoad.cpp

## Purpose
Handles parsing of terrain road definitions from INI files for the game engine.

## Responsibilities
- Parses INI entries for terrain road types
- Validates road definitions (e.g., prevents redefining bridges as roads)
- Creates or updates road type objects in the terrain road system
- Handles error conditions during parsing

## Key Types
- `INI` (Class): INI file parsing utility
- `TerrainRoadType` (Class): Represents a terrain road type
- `AsciiString` (Class): String handling utility

## Key Functions
### `parseTerrainRoadDefinition`
- Purpose: Parses a terrain road definition from an INI file
- Calls:
  - `ini->getNextToken()`
  - `TheTerrainRoads->findRoad()`
  - `TheTerrainRoads->newRoad()`
  - `ini->initFromINI()`
  - `road->getRoadFieldParse()`

## Globals
- `TheTerrainRoads` (External): Global terrain road manager instance

## Dependencies
- `PreRTS.h`
- `Common/INI.h`
- `GameClient/TerrainRoads.h`
