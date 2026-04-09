# Generals/Code/GameEngine/Source/Common/INI/INIDrawGroupInfo.cpp

## Purpose
This file contains functions and definitions for parsing INI entries related to `DrawGroupInfo`, which likely manages drawing group configurations in the game.

## Responsibilities
- Parsing integer values from INI files.
- Parsing percentage values to real numbers.
- Defining field parsing tables for `DrawGroupInfo`.
- Initializing `DrawGroupInfo` from INI data.

## Key Types
- None

## Key Functions
### parseInt
- Purpose: Parses an integer value and sets it in the appropriate field of a `DrawGroupInfo` object.
- Calls: `INI::parseInt`

### parsePercentToReal
- Purpose: Parses a percentage value to a real number and sets it in the appropriate field of a `DrawGroupInfo` object.
- Calls: `INI::parsePercentToReal`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "GameClient/DrawGroupInfo.h"
- External symbols used but not defined here:
  - `TheDrawGroupInfo`
  - `INI_UNKNOWN_ERROR`
