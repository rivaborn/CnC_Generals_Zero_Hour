# GeneralsMD/Code/GameEngine/Include/Common/MapObject.h

## Purpose
Defines the `MapObject` class, which encapsulates height map objects in the game world, including their properties, rendering, and runtime behavior.

## Responsibilities
- Manages map object properties (location, angle, flags, etc.)
- Handles rendering and shadow objects
- Provides access to object templates and waypoints
- Maintains linked list of map objects
- Validates object state (team, unique ID)

## Key Types
- **WorldHeightMapInterfaceClass (Class)**: Interface for seismic velocity access.
- **MapObject (Class)**: Core class representing game world objects.
- **WaypointID (Enum)**: Identifies waypoints.
- **FLAG_* (Enums)**: Bit flags for object properties (roads, bridges, rendering).
- **MO_* (Enums)**: Runtime flags (selected, light, waypoint, scorch).

## Key Functions
### `duplicate`
- Purpose: Creates a copy of the map object.
- Calls: Not inferable.

### `validate`
- Purpose: Validates object state (team and unique ID).
- Calls: `verifyValidTeam`, `verifyValidUniqueID`.

### `verifyValidTeam`
- Purpose: Ensures object is on a valid team.
- Calls: Not inferable.

### `verifyValidUniqueID`
- Purpose: Ensures object has a unique ID.
- Calls: Not inferable.

## Globals
- **TheMapObjectListPtr (MapObject*)**: Head of the map object linked list.
- **TheWorldDict (Dict)**: Global dictionary for world properties.

## Dependencies
- `Common/Dict.h`, `Common/GameMemory.h`, `GameClient/TerrainRoads.h`
- `Coord3D`, `AsciiString`, `Real`, `Int`, `Bool`, `MemoryPoolObject`
