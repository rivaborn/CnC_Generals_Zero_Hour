# GeneralsMD/Code/GameEngine/Include/Common/Handicap.h

## Purpose
Defines the Handicap class, which manages game balance modifiers for units and buildings.

## Responsibilities
- Stores handicap multipliers for build cost and time
- Provides methods to retrieve handicaps based on object type
- Initializes and reads handicap values from configuration data

## Key Types
- **Handicap (Class)**: Manages game balance modifiers
- **HandicapType (Enum)**: Defines handicap types (BUILDCOST, BUILDTIME)
- **ThingType (Enum)**: Defines object categories (GENERIC, BUILDINGS)

## Key Functions
### Handicap::init
- Purpose: Resets all handicaps to default values
- Calls: None

### Handicap::readFromDict
- Purpose: Initializes handicap values from configuration data
- Calls: None

### Handicap::getHandicap
- Purpose: Returns the multiplier for a given handicap type on an object
- Calls: getBestThingType

### Handicap::getBestThingType
- Purpose: Determines the most specific object type for a template
- Calls: None

## Globals
- None

## Dependencies
- BaseType.h
- Object, Dict, ThingTemplate (forward declarations)
