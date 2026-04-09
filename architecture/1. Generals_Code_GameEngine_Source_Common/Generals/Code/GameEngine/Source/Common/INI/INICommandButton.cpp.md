# Generals/Code/GameEngine/Source/Common/INI/INICommandButton.cpp

## Purpose
This file handles parsing command button definitions from INI files and managing their integration into the game's control bar.

## Responsibilities
- Parsing command button definitions from INI files.
- Managing the creation and updating of command buttons in the control bar.
- Handling duplicate command button entries with appropriate error handling or override logic.

## Key Types
- None

## Key Functions
### parseCommandButtonDefinition (INI *ini)
- Purpose: Parses a command button definition from an INI file.
- Calls:
  - `ControlBar::parseCommandButtonDefinition(ini)`
  - `TheControlBar->findNonConstCommandButton(name)`
  - `TheControlBar->newCommandButton(name)`
  - `button->markAsOverride()`
  - `DEBUG_CRASH(...)`

### parseCommandButtonDefinition (INI *ini)
- Purpose: Parses a command button definition from an INI file and manages its integration into the control bar.
- Calls:
  - `ini->getNextToken()`
  - `TheControlBar->findNonConstCommandButton(name)`
  - `TheControlBar->newCommandButton(name)`
  - `button->markAsOverride()`
  - `DEBUG_CRASH(...)`
  - `ini->initFromINI(button, button->getFieldParse())`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "GameClient/ControlBar.h"
