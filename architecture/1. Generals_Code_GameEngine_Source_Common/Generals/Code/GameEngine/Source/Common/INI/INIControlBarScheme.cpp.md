# Generals/Code/GameEngine/Source/Common/INI/INIControlBarScheme.cpp

## Purpose
This file contains the implementation for parsing control bar schemes from INI files in Command & Conquer Generals.

## Responsibilities
- Parse control bar scheme definitions from INI files.
- Manage and allocate control bar schemes using a manager.

## Key Types
- None

## Key Functions
### parseControlBarSchemeDefinition
- Purpose: Parses a control bar scheme definition from an INI file.
- Calls:
  - `getNextToken`
  - `set` (AsciiString)
  - `getControlBarSchemeManager` (ControlBar)
  - `newControlBarScheme` (ControlBarSchemeManager)
  - `initFromINI` (INI)

## Globals
- None

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "GameClient/ControlBar.h"
  - "GameClient/ControlBarScheme.h"
