# Generals/Code/GameEngine/Source/Common/INI/INIObject.cpp

## Purpose
This file contains functions for parsing object definitions from INI files in the Command & Conquer Generals game engine.

## Responsibilities
- Parse object entries from INI files.
- Handle reskinning of objects by parsing specific INI entries.

## Key Types
- None

## Key Functions
### parseObjectDefinition
- Purpose: Parses a standard object definition from an INI file.
- Calls: getNextToken, ThingFactory::parseObjectDefinition

### parseObjectReskinDefinition
- Purpose: Parses a reskinned object definition from an INI file.
- Calls: getNextToken, ThingFactory::parseObjectDefinition

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - "Common/INI.h"
  - "Common/ThingTemplate.h"
  - "Common/ThingFactory.h"
  - "GameLogic/Module/OpenContain.h"
