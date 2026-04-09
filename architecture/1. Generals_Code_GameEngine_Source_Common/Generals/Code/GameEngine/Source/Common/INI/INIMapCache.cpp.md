# Generals/Code/GameEngine/Source/Common/INI/INIMapCache.cpp

## Purpose
This file contains the implementation for parsing MapCache INI entries, which store metadata about maps in the game.

## Responsibilities
- Parses map metadata from INI files.
- Manages supply and tech positions as coordinate lists.
- Initializes `MapMetaData` objects with parsed data.

## Key Types
- **MapMetaDataReader (Class)**: Reads and stores map metadata fields.

## Key Functions
### parseSupplyPositionCoord3D
- Purpose: Parses a supply position coordinate from an INI file and adds it to the list in `MapMetaDataReader`.
- Calls: `INI::parseCoord3D`

### parseTechPositionsCoord3D
- Purpose: Parses a tech position coordinate from an INI file and adds it to the list in `MapMetaDataReader`.
- Calls: `INI::parseCoord3D`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Lib/BaseType.h"
  - "Common/INI.h"
  - "GameClient/MapUtil.h"
  - "GameNetwork/NetworkDefs.h"
  - "Common/NameKeyGenerator.h"
  - "Common/WellKnownKeys.h"
  - "Common/QuotedPrintable.h"
