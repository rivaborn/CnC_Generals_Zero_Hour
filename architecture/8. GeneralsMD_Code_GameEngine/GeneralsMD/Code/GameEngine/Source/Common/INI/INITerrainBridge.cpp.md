# GeneralsMD/Code/GameEngine/Source/Common/INI/INITerrainBridge.cpp

## Purpose
Parses terrain bridge definitions from INI files for the game's terrain system.

## Responsibilities
- Parses bridge entries from INI files
- Validates bridge definitions
- Creates new bridge objects via TerrainRoads manager
- Handles INI data loading for bridge properties

## Key Types
- `INI` (Class): INI file parsing utility
- `TerrainRoadType` (Class): Base class for terrain roads/bridges
- `AsciiString` (Class): String handling utility

## Key Functions
### `parseTerrainBridgeDefinition`
- Purpose: Parses a single terrain bridge definition from an INI file
- Calls: `ini->getNextToken()`, `TheTerrainRoads->findBridge()`, `TheTerrainRoads->newBridge()`, `ini->initFromINI()`, `bridge->getBridgeFieldParse()`

## Globals
- `TheTerrainRoads` (TerrainRoads*): Global terrain roads manager instance

## Dependencies
- `PreRTS.h` (include)
- `Common/INI.h` (include)
- `GameClient/TerrainRoads.h` (include)
- `DEBUG_ASSERTCRASH` macro
- `INI_INVALID_DATA` exception
