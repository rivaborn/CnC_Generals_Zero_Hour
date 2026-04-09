# Generals/Code/Tools/WorldBuilder/src/PolygonTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the polygon editing tool for WorldBuilder, bridging the gap between the map editor UI and the game's polygon trigger system. It handles user input, visual feedback, and undo/redo operations for polygon modifications.

## Cross-References
### Incoming
- `CWorldBuilderDoc` calls `deleteSelectedPolygon`, `mouseMoved`, and other functions during document operations
- `WbView` invokes `pickPolygon` and `poly_pickPoint` for selection logic
- `Tool` base class calls `setCursor` and `mouseMoved` during tool activation

### Outgoing
- Calls into `PolygonTrigger` for trigger management and point operations
- Uses `CUndoable` derivatives for undo/redo functionality
- Interacts with `WaypointOptions` for UI synchronization
- Depends on `WHeightMapEdit` for terrain operations

## Design Patterns
- **Command Pattern**: Uses `CUndoable` derivatives (`AddPolygonPointUndoable`, `DeletePolygonUndoable`) to encapsulate operations for undo/redo
- **State Pattern**: Tracks editing states (`m_poly_isAdding`, `m_poly_dragPointNdx`) to modify behavior dynamically
- **Strategy Pattern**: Different cursor behaviors (`m_poly_plusCursor`, `m_poly_moveCursor`) selected based on current operation

*Not inferable*: Exact implementation of snapping logic or polygon point insertion algorithm.
