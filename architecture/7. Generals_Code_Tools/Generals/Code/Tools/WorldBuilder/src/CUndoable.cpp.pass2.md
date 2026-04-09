# Generals/Code/Tools/WorldBuilder/src/CUndoable.cpp - Enhanced Analysis

## Architectural Role
This file implements the undo/redo system for WorldBuilder, a critical tool for map editing. It bridges the gap between user actions and persistent map state, ensuring non-destructive editing through a command pattern implementation.

## Cross-References
### Incoming
- **WorldBuilderDoc.cpp**: Likely pushes undo operations onto a stack when edits occur
- **Tool classes (PointerTool, RoadTool)**: Generate undoable actions during map modifications
- **WbView3D.cpp**: May trigger undo/redo operations via UI commands

### Outgoing
- **GameLogic/PolygonTrigger.cpp**: Modifies polygon triggers during undo/redo
- **GameLogic/SidesList.cpp**: Updates build lists when objects are offset
- **W3DDevice/GameClient/HeightMap.cpp**: Applies heightmap changes
- **LayersList.cpp**: Manages layer visibility during object operations

## Design Patterns
- **Command Pattern**: Encapsulates operations as Undoable objects for deferred execution
- **Memento Pattern**: Captures and restores internal state (e.g., heightmap data)
- **Composite Pattern**: Links multiple Undoable objects into a chain for batch operations

*Not inferable*: Exact relationship with SAGE engine's rendering pipeline or networking components.
