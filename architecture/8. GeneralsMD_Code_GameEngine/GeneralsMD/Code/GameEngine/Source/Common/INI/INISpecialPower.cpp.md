# GeneralsMD/Code/GameEngine/Source/Common/INI/INISpecialPower.cpp

## Purpose
Parses special power definitions from INI files for the game engine.

## Responsibilities
- Delegates INI parsing for special powers to `SpecialPowerStore`
- Handles file-level INI parsing logic
- Provides bridge between INI system and special power system

## Key Types
None

## Key Functions
### parseSpecialPowerDefinition
- Purpose: Parses special power definitions from an INI file
- Calls: `SpecialPowerStore::parseSpecialPowerDefinition`

## Globals
None

## Dependencies
- `PreRTS.h` (header guard)
- `Common/INI.h` (INI parsing interface)
- `Common/SpecialPower.h` (special power definitions)
- `SpecialPowerStore` class (external parser implementation)
