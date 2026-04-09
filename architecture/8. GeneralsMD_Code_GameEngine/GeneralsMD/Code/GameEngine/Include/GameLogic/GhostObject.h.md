# GeneralsMD/Code/GameEngine/Include/GameLogic/GhostObject.h

## Purpose
Manages "ghost" objectsâplaceholders for deleted objects that remain visible in fogged areas.

## Responsibilities
- Maintains snapshots of deleted objects for fogged visibility
- Handles parent object updates and partition data management
- Provides access to geometry and position data of ghost objects
- Manages ghost object lifecycle (addition/removal)
- Supports serialization (CRC, Xfer, loadPostProcess)

## Key Types
- **GhostObject (Class)**: Represents a ghosted object with snapshot capabilities
- **GhostObjectManager (Class)**: Singleton manager for ghost objects
- **GeometryType (Enum)**: Not inferable
- **ObjectID (Enum)**: Not inferable
- **Object (Class)**: Parent object reference
- **PartitionData (Class)**: Spatial partitioning data

## Key Functions
### GhostObject::snapShot
- Purpose: Captures object state for a specific player
- Calls: Not inferable

### GhostObjectManager::addGhostObject
- Purpose: Adds a new ghost object to the manager
- Calls: Not inferable

### GhostObjectManager::updateOrphanedObjects
- Purpose: Updates ghost objects whose parents were deleted
- Calls: Not inferable

### GhostObjectManager::releasePartitionData
- Purpose: Saves partition data for later restoration
- Calls: Not inferable

## Globals
- **TheGhostObjectManager (GhostObjectManager*)**: Singleton instance of the ghost object manager

## Dependencies
- `Lib/BaseType.h` (Base types)
- `Common/Snapshot.h` (Snapshot inheritance)
- `Xfer` (Serialization)
- `Coord3D` (3D coordinate)
- `Real`, `Bool`, `Int` (Base types)
