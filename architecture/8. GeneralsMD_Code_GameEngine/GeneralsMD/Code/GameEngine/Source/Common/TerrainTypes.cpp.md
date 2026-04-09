# GeneralsMD/Code/GameEngine/Source/Common/TerrainTypes.cpp

## Purpose
Manages terrain type definitions and their collection for the game engine.

## Responsibilities
- Defines terrain type properties via INI parsing
- Provides terrain type lookup and creation
- Maintains a global collection of terrain types
- Handles memory management for terrain types

## Key Types
- **TerrainType (Class)**: Represents a single terrain type with properties like texture and class
- **TerrainTypeCollection (Class)**: Manages a linked list of terrain types
- **m_terrainTypeFieldParseTable (const FieldParse[])**: INI parsing rules for terrain types

## Key Functions
### `findTerrain`
- Purpose: Finds a terrain type by name
- Calls: None

### `newTerrain`
- Purpose: Creates a new terrain type with default values
- Calls: `findTerrain`, `newInstance`

## Globals
- **TheTerrainTypes (TerrainTypeCollection*)**: Global pointer to the terrain type collection

## Dependencies
- `PreRTS.h`, `INI.h`, `TerrainTypes.h`
- `AsciiString`, `INI::parseAsciiString`, `INI::parseBool`, `INI::parseIndexList`
