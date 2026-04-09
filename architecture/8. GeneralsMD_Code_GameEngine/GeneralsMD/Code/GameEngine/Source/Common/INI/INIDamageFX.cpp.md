# GeneralsMD/Code/GameEngine/Source/Common/INI/INIDamageFX.cpp

## Purpose
Parses DamageFX definitions from INI files for the game engine.

## Responsibilities
- Parses DamageFX INI entries
- Delegates parsing to DamageFXStore
- Handles INI file reading for damage effects

## Key Types
- None

## Key Functions
### INI::parseDamageFXDefinition
- Purpose: Parses DamageFX definitions from an INI file
- Calls: DamageFXStore::parseDamageFXDefinition

## Globals
- None

## Dependencies
- "PreRTS.h"
- "Common/INI.h"
- "Common/DamageFX.h"
- DamageFXStore class
