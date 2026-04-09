# Generals/Code/GameEngine/Source/Common/INI/INI.cpp

## Purpose
This file contains the implementation of an INI (Initialization) reader for the Command & Conquer Generals game engine. It handles parsing INI files, managing file loading, and processing different types of data blocks defined within these files.

## Responsibilities
- Load and parse INI files.
- Validate filenames.
- Handle different data block types such as "AIData", "Animation", etc.
- Provide utility functions for scanning and converting data from strings to various types (e.g., integers, reals).

## Key Types
- **BlockParse (Class)**: Represents a mapping between a token string and its corresponding parsing function.

## Key Functions
### loadDirectory
- Purpose: Loads all INI files in the specified directory and subdirectories.
- Calls:
  - `getFileListInDirectory`
  - `load`

### findBlockParse
- Purpose: Finds the appropriate parsing function for a given block token.
- Calls: None

### findFieldParse
- Purpose: Finds the field parser for a given token within a parse table.
- Calls: None

### load
- Purpose: Loads and parses an INI file.
- Calls:
  - `prepFile`
  - `readLine`
  - `findBlockParse`
  - `(*parse)( this )`

## Globals
- **s_xfer (Xfer \*)**: Pointer to a transfer object used in parsing.
- **theTypeTable (const BlockParse[])**: Array of block types and their corresponding parsing functions.

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "Common/INIException.h"
  - "Common/DamageFX.h"
  - "Common/File.h"
  - "Common/FileSystem.h"
  - "Common/GameAudio.h"
  - "Common/Science.h"
  - "Common/SpecialPower.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Upgrade.h"
  - "Common/Xfer.h"
  - "Common/XferCRC.h"
  - "GameClient/Anim2D.h"
  - "GameClient/Color.h"
  - "GameClient/FXList.h"
  - "GameClient/GameText.h"
  - "GameClient/Image.h"
  - "GameClient/ParticleSys.h"
  - "GameLogic/Armor.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/FPUControl.h"
  - "GameLogic/ObjectCreationList.h"
  - "GameLogic/Weapon.h"

- External symbols used:
  - `TheFileSystem`
  - `TheScienceStore`
  - `TheVeterancyNames`
  - `TheDamageNames`
  - `TheDeathNames`
