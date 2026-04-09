# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DockUpdate.h

## Purpose
Defines the base class for docking behavior in the game, managing approach positions, docking states, and interactions with docking objects.

## Responsibilities
- Manages docking approach positions and reservations
- Controls docking state transitions (approach, enter, dock, exit)
- Handles dock open/closed status and passthrough permissions
- Provides position queries for docking path points
- Supports dynamic approach vector sizing

## Key Types
- DockUpdateModuleData (Class): Module data containing docking configuration
- DockUpdate (Class): Base class for docking behavior with position management
- DEFAULT_APPROACH_VECTOR_SIZE (Enum): Default size for approach vectors
- DYNAMIC_APPROACH_VECTOR_FLAG (Enum): Flag indicating dynamic vector sizing

## Key Functions
### isClearToApproach
- Purpose: Checks if docking approach is allowed
- Calls: Not inferable

### reserveApproachPosition
- Purpose: Reserves an approach position for a docker
- Calls: Not inferable

### advanceApproachPosition
- Purpose: Advances to next approach position
- Calls: Not inferable

### isClearToEnter
- Purpose: Checks if docking enter is allowed
- Calls: Not inferable

### update
- Purpose: Handles docking state transitions
- Calls: Not inferable

### loadDockPositions
- Purpose: Loads docking positions from drawable
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/INI.h
- Common/GameMemory.h
- Common/STLTypedefs.h
- GameLogic/Module/UpdateModule.h
