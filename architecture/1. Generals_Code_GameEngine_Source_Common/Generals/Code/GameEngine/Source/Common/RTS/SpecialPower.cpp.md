# Generals/Code/GameEngine/Source/Common/RTS/SpecialPower.cpp

## Purpose
This file manages special power templates and the system that holds them, including parsing definitions from INI files and checking if objects can use these powers.

## Responsibilities
- Parse special power definitions from INI files.
- Manage a store of special power templates.
- Check if an object meets the requirements to use a special power.
- Reset the special power store.

## Key Types
- SpecialPowerStore (Class): Manages special power templates.
- SpecialPowerTemplate (Class): Represents a template for a special power.
- SpecialPowerMaskType (Enum): Defines types of special powers.

## Key Functions
### parseSpecialPowerDefinition
- Purpose: Parses a special power definition from an INI file.
- Calls:
  - `ini->getNextToken()`
  - `findSpecialPowerTemplatePrivate()`
  - `newInstance(SpecialPowerTemplate)`
  - `ini->initFromINI()`

### canUseSpecialPower
- Purpose: Checks if an object can use a special power based on requirements.
- Calls:
  - `obj->getSpecialPowerModule()`
  - `obj->getControllingPlayer()`
  - `player->hasScience()`

## Globals
- TheSpecialPowerStore (SpecialPowerStore*): Global instance of the special power store.

## Dependencies
- Key includes:
  - "Common/Player.h"
  - "Common/Science.h"
  - "Common/SpecialPower.h"
  - "GameLogic/Object.h"
  - "Common/BitFlagsIO.h"
