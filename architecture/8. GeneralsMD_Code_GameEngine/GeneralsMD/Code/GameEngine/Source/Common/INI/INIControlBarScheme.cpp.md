# GeneralsMD/Code/GameEngine/Source/Common/INI/INIControlBarScheme.cpp

## Purpose
Parses control bar scheme definitions from INI files for the game's UI system.

## Responsibilities
- Parses INI data into ControlBarScheme objects
- Manages ControlBarScheme allocation via ControlBarSchemeManager
- Handles token-based INI parsing for UI components

## Key Types
- None (uses external types)

## Key Functions
### parseControlBarSchemeDefinition
- Purpose: Parses a control bar scheme definition from an INI file
- Calls:
  - INI::getNextToken()
  - ControlBarSchemeManager::newControlBarScheme()
  - INI::initFromINI()
  - ControlBarSchemeManager::getFieldParse()

## Globals
- None

## Dependencies
- "Common/INI.h"
- "GameClient/ControlBar.h"
- "GameClient/ControlBarScheme.h"
- "PreRTS.h"
- TheControlBar (external global)
- AsciiString (external type)
- DEBUG_ASSERTCRASH (external macro)
