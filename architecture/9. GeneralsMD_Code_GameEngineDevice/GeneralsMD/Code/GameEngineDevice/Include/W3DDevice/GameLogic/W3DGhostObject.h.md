# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameLogic/W3DGhostObject.h

## Purpose
Manages placeholder objects for deleted game entities that remain visible in fogged areas.

## Responsibilities
- Maintains ghost objects for entities hidden by fog of war
- Handles snapshots and scene updates for ghosted objects
- Manages object lifecycle (addition/removal/release)
- Tracks parent-child relationships for ghosted objects

## Key Types
- **W3DGhostObject (Class)**: Represents a ghosted game object with snapshot and scene management
- **W3DGhostObjectManager (Class)**: Manages collection of ghost objects and their lifecycle
- **W3DRenderObjectSnapshot (Class)**: Stores snapshot data for ghosted objects (forward declared)
- **PartitionData (Class)**: Contains partition data for ghosted objects (forward declared)
- **GhostObject (Class)**: Base class for ghost object functionality

## Key Functions
### W3DGhostObject::snapShot
- Purpose: Creates a snapshot of the object for a specific player
- Calls: Not inferable

### W3DGhostObject::updateParentObject
- Purpose: Updates the parent object reference and partition data
- Calls: Not inferable

### W3DGhostObjectManager::addGhostObject
- Purpose: Adds a new ghost object to the manager
- Calls: Not inferable

### W3DGhostObjectManager::updateOrphanedObjects
- Purpose: Updates ghost objects that have lost their parent objects
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/GhostObject.h` (base class)
- `Lib/BaseType.h` (base types)
- `Common/GameCommon.h` (game constants)
- `GameClient/DrawableInfo.h` (drawable information)
- Forward declarations: `Object
