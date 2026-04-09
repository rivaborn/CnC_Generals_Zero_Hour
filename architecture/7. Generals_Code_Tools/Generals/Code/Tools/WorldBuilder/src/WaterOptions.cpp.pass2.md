# Generals/Code/Tools/WorldBuilder/src/WaterOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the water/river editing UI in WorldBuilder, bridging the gap between user input and the underlying map data model. It manages the state of water areas and rivers, coordinating with the 3D view and undo system.

## Cross-References
### Incoming
- **WaypointOptions.cpp**: Calls `updateTheUI()` to refresh the water options panel when polygon selection changes
- **PolygonTool.cpp**: Likely invokes `setHeight()` during polygon creation/modification
- **WorldBuilderDoc.cpp**: Manages the undo stack containing `MovePolygonUndoable` instances created here

### Outgoing
- **PolygonTrigger.h**: Directly manipulates water/river polygon properties
- **WbView3d.h**: Triggers view invalidation after height changes
- **CUndoable.h**: Uses the undo framework for height adjustments
- **LayersList.h**: Accesses layer information for water placement

## Design Patterns
- **Singleton**: Uses `m_staticThis` for global access to the dialog instance
- **Observer**: Updates UI when underlying data changes (e.g., polygon selection)
- **Command**: Encapsulates water height changes in `MovePolygonUndoable` for undo/redo

Rules followed. Analysis limited to observable code behavior.
