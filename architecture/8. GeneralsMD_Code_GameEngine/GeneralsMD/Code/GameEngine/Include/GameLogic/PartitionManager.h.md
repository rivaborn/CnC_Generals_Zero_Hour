# GeneralsMD/Code/GameEngine/Include/GameLogic/PartitionManager.h

## Purpose
Header for the PartitionManager system, which handles spatial partitioning of game objects for efficient collision detection, spatial queries, and visibility management.

## Responsibilities
- Manages spatial partitioning of game objects
- Handles collision detection and spatial queries
- Manages visibility/shroud system
- Provides object iteration and filtering capabilities
- Maintains threat/value maps for AI decision making

## Key Types
- **PartitionManager (Class)**: Singleton managing spatial partitioning and collision system
- **PartitionCell (Class)**: Represents a spatial cell in the partition grid
- **PartitionData (Class)**: Object-specific partition data
- **PartitionFilter (Class)**: Base class for object filtering criteria
- **CellAndObjectIntersection (Class)**: Tracks intersections between objects and cells
- **FindPositionOptions (Struct)**: Options for finding valid positions in the world
- **SightingInfo (Class)**: Encapsulates visibility/sighting information
- **ShroudStatusStoreRestore (Struct)**: Stores/restores shroud state
- **DistanceCalculationType (Enum)**: Types of distance calculations
- **FindPositionFlags (Enum)**: Flags for position finding
- **ValueOrThreat (Enum)**: Types of value calculations

## Key Functions
### getClosestObjects
- Purpose: Finds closest objects matching filters within a range
- Calls: Internal cell iteration logic

### findPositionAround
- Purpose: Finds valid positions around a center point
- Calls: tryPosition, cell iteration functions

### doShroudReveal/doShroudCover
- Purpose: Manages visibility shroud operations
- Calls: Internal cell iteration and shroud update logic

### iterateObjectsInRange
- Purpose: Iterates objects within a range with optional filters
- Calls: Internal cell iteration and filtering logic

### getShroudStatusForPlayer
- Purpose: Gets shroud status for a player at a location
- Calls: Cell lookup and shroud status queries

## Globals
- **ThePartitionManager (PartitionManager*)**: Singleton instance
- **HUGE_DIST (Real)**: Large distance constant
- **RANDOM_START_ANGLE (Real)**: Special angle value

## Dependencies
- Common/GameCommon.h
- GameLogic/ObjectIter.h
- Common/ObjectStatusTypes.h
- Common/KindOf.h
- Common/Snapshot.h
- Common/Geometry.h
- GameClient/Display.h
