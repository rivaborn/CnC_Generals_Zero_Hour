# Generals/Code/Tools/WorldBuilder/include/WaypointOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI dialog for waypoint editing in WorldBuilder, bridging the gap between the map editor's selection system and the underlying waypoint/polygon data model. It provides both the dialog implementation and static utility functions used by other tools for waypoint management.

## Cross-References
### Incoming
- **WorldBuilder UI controllers**: Call static methods like `getSingleSelectedWaypoint` and `update` to synchronize selection state.
- **Undo/Redo system**: Likely uses `MovePolygonUndoable` for tracking waypoint position changes.
- **Map object selection system**: Relies on `getSingleSelectedPolygon` for trigger management.

### Outgoing
- **OptionsPanel base class**: Inherits UI behavior and DDX/DDV handling.
- **Map object system**: Interacts with `MapObject` and `PolygonTrigger` instances.
- **Name key system**: Uses `WellKnownKeys.h` for waypoint label management.

## Design Patterns
- **Singleton-like access**: Static `m_staticThis` provides global access to the dialog instance.
- **Observer pattern**: `updateTheUI` and `update` methods suggest a push-based UI refresh mechanism.
- **Factory method**: `GenerateUniqueName` encapsulates naming logic for waypoint creation.
