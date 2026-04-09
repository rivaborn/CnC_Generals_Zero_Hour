# GeneralsMD/Code/GameEngine/Source/GameClient/Terrain/TerrainRoads.cpp

## Purpose
Manages terrain road and bridge descriptions, including parsing INI data and maintaining collections of road types.

## Responsibilities
- Parses INI configuration for road/bridge properties
- Manages collections of road and bridge types
- Provides lookup and iteration methods for road/bridge data
- Handles damage/repair state transitions for bridges

## Key Types
- **TerrainRoadType (Class)**: Represents a road or bridge type with properties like texture, width, and damage states
- **TerrainRoadCollection (Class)**: Manages collections of road and bridge types
- **FieldParse (Struct)**: Used for INI field parsing definitions

## Key Functions
### `parseTransitionToOCL`
- Purpose: Parses OCL transition effects for bridge damage/repair states
- Calls: `ini->getNextSubToken`, `ini->scanIndexList`, `ini->scanInt`, `friend_setDamageToOCLString`, `friend_setRepairedToOCLString`

### `parseTransitionToFX`
- Purpose: Parses FX transition effects for bridge damage/repair states
- Calls: `ini->getNextSubToken`, `ini->scanIndexList`, `ini->scanInt`, `friend_setDamageToFXString`, `friend_setRepairedToFXString`

### `findRoadOrBridge`
- Purpose: Searches both road and bridge lists for a matching name
- Calls: `findRoad`, `findBridge`

### `newRoad` / `newBridge`
- Purpose: Creates new road/bridge instances with default values
- Calls: `newInstance`, `friend_setName`, `friend_setID`, etc.

## Globals
- **TheTerrainRoads (TerrainRoadCollection*)**: Global instance of the terrain road collection

## Dependencies
- `PreRTS.h`, `Common/INI.h`, `GameClient/TerrainRoads.h`
- `INI` class for parsing
- `AsciiString` for string handling
- `BodyDamageType` enum for damage states
