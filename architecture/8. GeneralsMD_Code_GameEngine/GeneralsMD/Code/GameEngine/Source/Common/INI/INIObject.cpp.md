# GeneralsMD/Code/GameEngine/Source/Common/INI/INIObject.cpp

## Purpose
Parses object and reskin definitions from INI files for the game engine.

## Responsibilities
- Parses object definitions from INI entries
- Parses reskin definitions from INI entries
- Delegates parsing to ThingFactory
- Handles token extraction from INI files

## Key Types
None

## Key Functions
### INI::parseObjectDefinition
- Purpose: Parses an object definition from an INI file.
- Calls: `ini->getNextToken()`, `ThingFactory::parseObjectDefinition`

### INI::parseObjectReskinDefinition
- Purpose: Parses a reskin definition from an INI file.
- Calls: `ini->getNextToken()`, `ThingFactory::parseObjectDefinition`

## Globals
None

## Dependencies
- `PreRTS.h`
- `Common/INI.h`
- `Common/ThingTemplate.h`
- `Common/ThingFactory.h`
- `GameLogic/Module/OpenContain.h`
- `AsciiString` class
- `ThingFactory` class
