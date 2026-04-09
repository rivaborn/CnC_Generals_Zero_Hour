# Generals/Code/Tools/WorldBuilder/include/PointerTool.h - Enhanced Analysis

## Architectural Role
This file defines the core interaction tool for WorldBuilder's object manipulation, bridging user input (mouse events) with the game's map editing functionality. It extends `PolygonTool`, indicating a hierarchical tool system where specialized tools inherit common behavior.

## Cross-References
### Incoming
- Likely called by WorldBuilder's view/system classes handling mouse events (e.g., `WbView`, `CWorldBuilderDoc`).
- `ModifyObjectUndoable` instances are created/managed here, implying undo/redo system integration.

### Outgoing
- Calls into `PolygonTool` base class methods (inheritance).
- Interacts with `MapObject` for selection/manipulation logic.
- Uses `WorldHeightMapEdit` for terrain modifications (indirectly via `PolygonTool`).

## Design Patterns
- **Template Method**: Mouse event handlers (`mouseDown`, `mouseMoved`, `mouseUp`) define a workflow that subclasses can extend.
- **State Pattern**: Internal flags (`m_moving`, `m_rotating`) represent tool states, altering behavior dynamically.
- **Observer**: Cursor changes (`setCursor`) suggest event-driven UI updates (not explicitly shown but implied by cursor state tracking).
