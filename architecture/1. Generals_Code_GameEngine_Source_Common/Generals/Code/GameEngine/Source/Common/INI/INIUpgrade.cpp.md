# Generals/Code/GameEngine/Source/Common/INI/INIUpgrade.cpp

## Purpose
This file contains the implementation for parsing upgrade definitions from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parses upgrade definitions from INI files.
- Utilizes the `UpgradeCenter` class to handle the parsing logic.

## Key Types
- None

## Key Functions
### parseUpgradeDefinition
- Purpose: Parses an upgrade definition from an INI file.
- Calls: 
  - `UpgradeCenter::parseUpgradeDefinition(ini)`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "Common/Upgrade.h"
