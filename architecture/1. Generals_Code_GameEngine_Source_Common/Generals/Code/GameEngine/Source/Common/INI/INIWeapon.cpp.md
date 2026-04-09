# Generals/Code/GameEngine/Source/Common/INI/INIWeapon.cpp

## Purpose
This file contains the implementation for parsing weapon INI entries in the Command & Conquer Generals game engine.

## Responsibilities
- Parses weapon template definitions from INI files.
- Utilizes the `WeaponStore` class to handle parsed data.

## Key Types
- None

## Key Functions
### parseWeaponTemplateDefinition
- Purpose: Parses a weapon entry from an INI file.
- Calls: 
  - `WeaponStore::parseWeaponTemplateDefinition(ini)`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "GameLogic/Weapon.h"
