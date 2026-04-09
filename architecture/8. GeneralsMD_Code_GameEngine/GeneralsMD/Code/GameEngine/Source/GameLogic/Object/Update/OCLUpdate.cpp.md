# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/OCLUpdate.cpp

## Purpose
Handles periodic creation of objects via Object Creation Lists (OCL) for game entities.

## Responsibilities
- Parses faction-specific OCL configurations from INI files
- Manages timed object spawning based on module data
- Handles faction-triggered object creation logic
- Provides countdown and timing utilities for UI display

## Key Types
- `OCLUpdateModuleData` (Class): Stores configuration for OCL updates (delays, OCL references, faction settings)
- `OCLUpdate` (Class): Implements the update module behavior for timed object creation
- `FactionOCLInfo` (Struct): Pairs faction names with their associated OCLs

## Key Functions
### `parseFactionObjectCreationList`
- Purpose: Parses faction-specific OCL entries from INI files
- Calls: `INI::parseObjectCreationList`, `ini->getNextToken`, `ini->getNextTokenOrNull`

### `OCLUpdate::update`
- Purpose: Main update loop that handles timed object creation
- Calls: `TheTerrainLogic->findClosestEdgePoint`, `ObjectCreationList::create`, `shouldCreate`, `setNextCreationFrame`

### `OCLUpdate::shouldCreate`
- Purpose: Determines if it's time to create objects based on timers and object status
- Calls: `TheGameLogic->getFrame`, `getObject()->getStatusBits`

### `OCLUpdate::setNextCreationFrame`
- Purpose: Calculates and sets the next creation time based on random delay
- Calls: `GameLogicRandomValue`, `TheGameLogic->getFrame`

## Globals
- `TheTerrainLogic` (External): Used for edge point finding
- `TheGameLogic` (External): Used for frame timing

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`
- `GameLogic/ObjectCreationList.h`, `GameLogic/Module/OCLUpdate.h`
- `INI` class methods for parsing
- `UpdateModule` base class
- `ObjectCreationList` for actual object creation
