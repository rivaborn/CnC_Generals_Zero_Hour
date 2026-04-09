# GeneralsMD/Code/GameEngine/Source/Common/INI/INIWeapon.cpp

## Purpose
Parses weapon template definitions from INI files for the game engine.

## Responsibilities
- Parses weapon-related INI entries
- Delegates parsing to WeaponStore class
- Handles INI file format for weapon data

## Key Types
- None

## Key Functions
### parseWeaponTemplateDefinition
- Purpose: Parses weapon template definitions from an INI file
- Calls: WeaponStore::parseWeaponTemplateDefinition

## Globals
- None

## Dependencies
- "PreRTS.h" (must be first include)
- "Common/INI.h"
- "GameLogic/Weapon.h"
- WeaponStore class methods
