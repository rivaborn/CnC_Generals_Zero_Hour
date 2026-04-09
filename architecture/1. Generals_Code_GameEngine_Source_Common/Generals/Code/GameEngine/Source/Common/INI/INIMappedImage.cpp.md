# Generals/Code/GameEngine/Source/Common/INI/INIMappedImage.cpp

## Purpose
This file contains the implementation for parsing mapped image entries from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parsing mapped image definitions from INI files.
- Managing the creation and initialization of `Image` objects based on parsed data.
- Ensuring that existing images are not overwritten with new data.

## Key Types
- None

## Key Functions
### parseMappedImageDefinition
- Purpose: Parses a mapped image entry from an INI file and initializes or updates an `Image` object accordingly.
- Calls:
  - `getNextToken`
  - `set`
  - `findImageByName`
  - `newImage`
  - `setName`
  - `initFromINI`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "GameClient/Image.h"
