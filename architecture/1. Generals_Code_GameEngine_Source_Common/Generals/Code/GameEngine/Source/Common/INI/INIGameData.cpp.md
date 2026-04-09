# Generals/Code/GameEngine/Source/Common/INI/INIGameData.cpp

## Purpose
This file contains the implementation for parsing GameData entries from INI files.

## Responsibilities
- Parses GameData entries using the `parseGameDataDefinition` function.
- Utilizes the `GlobalData` class to handle parsed data.

## Key Types
- None

## Key Functions
### parseGameDataDefinition
- Purpose: Parses GameData entries from an INI file.
- Calls: 
  - GlobalData::parseGameDataDefinition(ini)

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "Common/GlobalData.h"
