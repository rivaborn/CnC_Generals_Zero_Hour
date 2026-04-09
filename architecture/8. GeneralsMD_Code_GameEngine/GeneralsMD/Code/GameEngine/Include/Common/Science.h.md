# GeneralsMD/Code/GameEngine/Include/Common/Science.h

## Purpose
Defines the science/technology system for the game, including science types, their prerequisites, and purchase costs.

## Responsibilities
- Manages science definitions and their relationships
- Provides methods to check science validity, prerequisites, and purchase eligibility
- Handles science name lookups and internal name conversions
- Tracks purchasable sciences for players

## Key Types
- **ScienceType (Enum)**: Science identifier type
- **ScienceVec (Class)**: Vector of ScienceType values
- **ScienceInfo (Class)**: Contains science metadata (name, description, prerequisites, cost)
- **ScienceStore (Class)**: Central manager for science system, handles initialization and queries

## Key Functions
### ScienceStore::isValidScience
- Purpose: Checks if a science type is valid
- Calls: findScienceInfo

### ScienceStore::playerHasPrereqsForScience
- Purpose: Determines if a player meets prerequisites for a science
- Calls: findScienceInfo

### ScienceStore::getPurchasableSciences
- Purpose: Returns sciences a player can purchase now and potentially in the future
- Calls: findScienceInfo

### ScienceStore::friend_lookupScience
- Purpose: Looks up science by name (internal use only)
- Calls: None

## Globals
- **TheScienceStore (ScienceStore*)**: Global instance of the science store

## Dependencies
- Common/Overridable.h
- Common/NameKeyGenerator.h
- Common/UnicodeString.h
- Player class
- INI class
- std::vector
