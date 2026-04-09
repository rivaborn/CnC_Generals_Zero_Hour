# GeneralsMD/Code/GameEngine/Source/Common/RTS/Science.cpp

## Purpose
Manages science/technology research system, including parsing, storage, and querying of science definitions.

## Responsibilities
- Stores and manages `ScienceInfo` objects
- Parses science definitions from INI files
- Provides lookup and validation for science types
- Determines purchasable sciences for players based on prerequisites

## Key Types
- `ScienceStore` (Class): Central manager for science data
- `ScienceInfo` (Class): Contains details about a specific science/technology
- `ScienceType` (Enum): Type-safe identifier for sciences

## Key Functions
### `ScienceStore::init()`
- Purpose: Clears all science data
- Calls: None

### `ScienceStore::findScienceInfo(ScienceType)`
- Purpose: Looks up science info by type
- Calls: None

### `ScienceStore::getPurchasableSciences(const Player*, ScienceVec&, ScienceVec&)`
- Purpose: Determines which sciences a player can purchase
- Calls: `playerHasPrereqsForScience`, `playerHasRootPrereqsForScience`

### `ScienceStore::friend_parseScienceDefinition(INI*)`
- Purpose: Parses science definitions from INI files
- Calls: `INI::parseScienceVector`, `INI::parseInt`, `INI::parseBool`, `INI::parseAndTranslateLabel`

## Globals
- `TheScienceStore` (ScienceStore*): Singleton instance of the science store

## Dependencies
- `INI.h` - For parsing configuration files
- `Player.h` - For player science state checks
- `Science.h` - For science type definitions
- `PreRTS.h` - Engine precompilation header
