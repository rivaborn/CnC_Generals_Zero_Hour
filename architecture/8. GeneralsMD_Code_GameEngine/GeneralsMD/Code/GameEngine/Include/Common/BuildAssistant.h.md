# GeneralsMD/Code/GameEngine/Include/Common/BuildAssistant.h

## Purpose
Header for the BuildAssistant class, which handles building and placement logic for structures and units in the game.

## Responsibilities
- Manages construction rules and validation
- Handles object placement and pathfinding
- Provides build location calculations
- Manages object selling mechanics
- Handles removable objects during construction

## Key Types
- **BuildAssistant (Class)**: Singleton class for build-related operations
- **ObjectSellInfo (Class)**: Stores information about objects being sold
- **CanMakeType (Enum)**: Return codes for buildability checks
- **LegalBuildCode (Enum)**: Return codes for build location validation
- **TileBuildInfo (Struct)**: Contains tile usage and position data for tiled builds

## Key Functions
### `isLocationLegalToBuild`
- Purpose: Checks if a location is valid for building
- Calls: Not inferable

### `canMakeUnit`
- Purpose: Determines if a unit can be produced
- Calls: Not inferable

### `buildObjectNow`
- Purpose: Instantly creates an object in the world
- Calls: Not inferable

### `isLocationClearOfObjects`
- Purpose: Checks if a location is clear of obstacles
- Calls: Not inferable

## Globals
- **TheBuildAssistant (BuildAssistant*)**: Singleton instance of BuildAssistant

## Dependencies
- `Common/STLTypedefs.h`
- `Lib/BaseType.h`
- `Common/SubsystemInterface.h`
- `GameLogic/Object.h`
- `ThingTemplate`, `Player`, `Object` (forward declarations)
