# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/OCLSpecialPower.cpp

## Purpose
This file implements the `OCLSpecialPower` class, which handles special powers driven by object creation lists in Command & Conquer Generals.

## Responsibilities
- Parses configuration data for special power upgrades.
- Determines the appropriate object creation list based on player science.
- Executes special powers at specified locations or objects.
- Manages CRC and Xfer operations for serialization.

## Key Types
- **(anonymous enum)**: Enumerates different creation location types.
- **CREATE_ABOVE_LOCATION_HEIGHT (Enum)**: Defines a height offset for creating objects above a location.

## Key Functions
### parseOCLUpgradePair
- Purpose: Parses an upgrade pair from an INI file, storing science and object creation list data.
- Calls: `INI::parseScience`, `INI::parseObjectCreationList`

### OCLSpecialPowerModuleData::buildFieldParse
- Purpose: Builds field parsing for special power module data.
- Calls: `SpecialPowerModuleData::buildFieldParse`

## Globals
- **TheOCLCreateLocTypeNames (const char\*\*)**: Array of strings representing different creation location types.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/ObjectCreationList.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/Module/OCLSpecialPower.h"
