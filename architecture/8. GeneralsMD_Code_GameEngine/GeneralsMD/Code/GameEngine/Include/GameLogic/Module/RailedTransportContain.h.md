# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RailedTransportContain.h

## Purpose
Defines the `RailedTransportContain` class, a module for managing rail-based transport containment logic in the game.

## Responsibilities
- Manages rail-specific transport containment behavior
- Handles object removal and exit logic for rail transports
- Provides rail-specific rider exit checks
- Inherits base transport containment functionality

## Key Types
- **RailedTransportContain (Class)**: Rail transport containment module
- **RailedTransportContainMagicEnum (Enum)**: Not inferable
- **RailedTransportContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### RailedTransportContain()
- Purpose: Constructor for rail transport containment module
- Calls: Not inferable

### onRemoving()
- Purpose: Handles object removal from rail transport
- Calls: Not inferable

### exitObjectViaDoor()
- Purpose: Exits object through specified door type
- Calls: Not inferable

### isSpecificRiderFreeToExit()
- Purpose: Checks if specific rider can exit rail transport
- Calls: Not inferable

## Globals
- None

## Dependencies
- `TransportContain.h` (base class)
- Memory pool and module macro utilities
- `Thing` and `Object` class types
