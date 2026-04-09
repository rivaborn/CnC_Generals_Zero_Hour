# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/GSConfig.cpp

## Purpose
Handles GameSpy online configuration parsing and management for Command & Conquer Generals Zero Hour.

## Responsibilities
- Parses GameSpy configuration file (XML-like format)
- Manages ping server settings, QM maps, VIP lists, NAT timeouts
- Provides access to configuration values via interface methods
- Handles section-based parsing with SectionChecker helper

## Key Types
- **GameSpyConfig (Class)**: Main configuration parser and storage class
- **SectionChecker (Class)**: Helper to track active parsing sections
- **SectionList (Class)**: Typedef for list of section flags

## Key Functions
### GameSpyConfig::GameSpyConfig
- Purpose: Constructor that initializes default values and parses config string
- Calls: SectionChecker methods, various string parsing methods

### GameSpyConfig::getPointsForRank
- Purpose: Returns points value for a given rank
- Calls: None

### GameSpyConfig::getManglerLocation
- Purpose: Retrieves mangler host/port by index
- Calls: None

### GameSpyConfig::isPlayerVIP
- Purpose: Checks if player ID is in VIP list
- Calls: std::find

## Globals
- **TheGameSpyConfig (GameSpyConfigInterface*)**: Global config interface instance

## Dependencies
- "PreRTS.h", "Common/GameState.h", "GameClient/MapUtil.h", "GameNetwork/GameSpy/GSConfig.h", "GameNetwork/RankPointValue.h"
- Uses std::list, std::vector, std::set, AsciiString, MapMetaData, DEBUG_LOG
