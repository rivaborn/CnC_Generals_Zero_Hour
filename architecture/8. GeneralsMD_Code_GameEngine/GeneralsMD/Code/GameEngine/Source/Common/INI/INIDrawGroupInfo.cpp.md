# GeneralsMD/Code/GameEngine/Source/Common/INI/INIDrawGroupInfo.cpp

## Purpose
Parses INI configuration entries for DrawGroupInfo, handling pixel/percent position values and other text-drawing properties.

## Responsibilities
- Parses integer and percent-to-real values for draw positions
- Configures DrawGroupInfo fields from INI data
- Handles pixel vs. percent offset flags

## Key Types
- **None**

## Key Functions
### parseInt
- Purpose: Parses integer draw position values and sets pixel offset flags
- Calls: INI::parseInt

### parsePercentToReal
- Purpose: Parses percent-based draw positions and sets percent offset flags
- Calls: INI::parsePercentToReal

### INI::parseDrawGroupNumberDefinition
- Purpose: Initializes DrawGroupInfo from INI data
- Calls: ini->initFromINI

## Globals
- **TheDrawGroupInfo** (DrawGroupInfo*): Global instance used for INI parsing

## Dependencies
- INI.h (INI class, parsing utilities)
- GameClient/DrawGroupInfo.h (DrawGroupInfo class)
- PreRTS.h (engine precompiled header)
