# Generals/Code/Tools/WorldBuilder/src/WaypointOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for waypoint and polygon trigger editing in WorldBuilder, bridging MFC UI controls with the game's map object system. It handles property synchronization between UI and map objects while enforcing naming constraints.

## Cross-References
### Incoming
- Called by MFC event handlers (e.g., `OnEditchangeWaypointlabel1Edit`) from the dialog's message map
- Used by `CWorldBuilderDoc` to update linked waypoint labels
- Accessed by `Tool` subclasses (e.g., `WaypointTool`) for selection state

### Outgoing
- Interacts with `MapObject` and `PolygonTrigger` for property updates
- Uses `CWorldBuilderDoc` for document state and validation
- Depends on `LayersList` for layer management
- References `NameKeyGenerator` for key-to-name conversion

## Design Patterns
- **Observer Pattern**: UI updates react to selection changes via `updateTheUI()`
- **Singleton**: `m_staticThis` provides global access to the dialog instance
- **Strategy Pattern**: Different UI behaviors for waypoints vs. polygon triggers (e.g., name validation logic diverges)

*Not inferable*: Exact undo/redo integration with `CUndoable` not shown in truncated content.
