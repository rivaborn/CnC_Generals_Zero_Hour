# GeneralsMD/Code/GameEngine/Source/Common/INI/INIGameData.cpp

## Purpose
Parses GameData entries from INI files for the game engine.

## Responsibilities
- Parses INI entries related to game data
- Delegates parsing to GlobalData module
- Provides public interface for INI parsing

## Key Types
None

## Key Functions
### parseGameDataDefinition
- Purpose: Parses GameData entry from INI file
- Calls: GlobalData::parseGameDataDefinition

## Globals
None

## Dependencies
- INI.h (header)
- GlobalData.h (header)
- PreRTS.h (header)
