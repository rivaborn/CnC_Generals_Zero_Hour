# Generals/Code/Tools/WorldBuilder/src/PointerTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the core interaction logic for the WorldBuilder editor's pointer tool, bridging user input (mouse events) with scene manipulation. It handles object selection, transformation, and waypoint management, acting as a controller in the MVC pattern for the editor's 3D view.

## Cross-References
### Incoming
- **WBView3D.h**: Uses `docToViewCoords`/`viewToDocCoords` for coordinate conversion
- **WorldBuilderDoc.h**: Accesses waypoint links and manages undo actions
- **PolygonTool.h**: Delegates polygon editing operations
- **ObjectTool.h**: Uses `calcAngle` for rotation calculations

### Outgoing
- **CUndoable.h**: Creates `ModifyObjectUndoable` for undo/redo support
- **MainFrm.h**: Triggers property panel updates via `showOptionsDialog`
- **MapObject.h**: Iterates through scene objects for selection/deselection

## Design Patterns
- **Command Pattern**: Encapsulates object modifications in `ModifyObjectUndoable` for undo/redo
- **Visitor Pattern**: Iterates over `MapObject` linked list for selection operations
- **State Pattern**: Cursor behavior changes based on tool state (rotate/move)

*Not inferable*: Exact observer implementation for view updates.
