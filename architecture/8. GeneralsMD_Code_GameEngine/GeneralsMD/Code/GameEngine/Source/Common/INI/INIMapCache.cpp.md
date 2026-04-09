# GeneralsMD/Code/GameEngine/Source/Common/INI/INIMapCache.cpp

## Purpose
Parses map metadata from INI files for the game's map cache system.

## Responsibilities
- Defines `MapMetaDataReader` class to hold parsed map data.
- Implements parsing functions for supply and tech positions.
- Provides a field parse table for INI parsing.
- Contains the main `parseMapCacheDefinition` function to process map INI entries.

## Key Types
- **MapMetaDataReader (Class)**: Holds parsed map metadata including extent, player count, positions, and file info.
- **None**: No other classes/structs/enums defined.

## Key Functions
### parseSupplyPositionCoord3D
- Purpose: Parses supply position coordinates from INI and adds them to the reader's supply positions list.
- Calls: `INI::parseCoord3D`

### parseTechPositionsCoord3D
- Purpose: Parses tech position coordinates from INI and adds them to the reader's tech positions list.
- Calls: `INI::parseCoord3D`

### INI::parseMapCacheDefinition
- Purpose: Main function to parse map cache INI entries and populate the map cache.
- Calls: `ini->getNextToken`, `ini->initFromINI`, `QuotedPrintableToAsciiString`, `TheNameKeyGenerator->keyToName`, `TheGameText->fetch`, `TheMapCache` access.

## Globals
- **MapMetaDataReader::m_mapFieldParseTable (FieldParse[])**: Parse table for INI field definitions.

## Dependencies
- Key includes: `PreRTS.h`, `Lib/BaseType.h`, `Common/INI.h`, `GameClient/MapUtil.h`, `GameClient/GameText.h`, `GameNetwork/NetworkDefs.h`, `Common/NameKeyGenerator.h`, `Common/WellKnownKeys.h`, `Common/QuotedPrintable.h`
- External symbols: `INI`, `Coord3D`, `Coord3DList`, `Region3D`, `MapMetaData`, `TheNameKeyGenerator`, `TheKey_InitialCameraPosition`, `TheGameText`, `TheMapCache`
