# Generals/Code/GameEngine/Source/Common/INI/INIAnimation.cpp

## Purpose
This file contains the implementation for parsing animation INI entries, specifically for 2D image animations in Command & Conquer Generals.

## Responsibilities
- Parses animation definitions from INI files.
- Manages the creation and initialization of `Anim2DTemplate` objects.
- Ensures that no duplicate animation templates are created.

## Key Types
- None

## Key Functions
### parseAnim2DDefinition
- Purpose: Parses an animation definition from an INI file and initializes an `Anim2DTemplate`.
- Calls:
  - `getNextToken`
  - `set` (AsciiString)
  - `findTemplate` (TheAnim2DCollection)
  - `newTemplate` (TheAnim2DCollection)
  - `initFromINI`

## Globals
- None

## Dependencies
- Key includes: "PreRTS.h", "Common/INI.h", "GameClient/Anim2D.h"
- External symbols used:
  - TheAnim2DCollection
  - DEBUG_ASSERTCRASH
  - DEBUG_CRASH
