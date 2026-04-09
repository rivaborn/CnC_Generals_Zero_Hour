# Generals/Code/Tools/WorldBuilder/src/RoadTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the road placement tool in WorldBuilder, bridging the gap between user input and map object manipulation. It handles the creation, modification, and connection of road segments while integrating with the undo/redo system and terrain snapping logic.

## Cross-References
### Incoming
- **WorldBuilderView**: Calls `mouseDown`, `mouseMoved`, `mouseUp` during tool interaction
- **PointerTool**: Uses `clearSelection` to manage object selection state
- **RoadOptions**: Queries current road settings (type, curvature) during placement

### Outgoing
- **MapObject**: Creates and manipulates road endpoint objects
- **CUndoable**: Uses `AddObjectUndoable`/`DeleteObjectUndoable` for undo/redo support
- **WbView**: Converts screen coordinates to world space via `viewToDocCoords`
- **TheThingFactory**: Retrieves road templates for new segments

## Design Patterns
- **Command Pattern**: Encapsulates road operations in undoable commands (`AddObjectUndoable`, `DeleteObjectUndoable`)
- **State Pattern**: Tool behavior changes based on mouse interaction state (down/moved/up)
- **Flyweight Pattern**: Reuses road templates from `TheThingFactory` rather than creating new ones

*Not inferable*: No clear use of Observer or Strategy patterns despite tool activation logic.
