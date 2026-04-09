# Generals/Code/Tools/WorldBuilder/src/BrushTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the core terrain editing functionality in WorldBuilder, serving as the bridge between user input and heightmap modifications. It encapsulates the brush tool's state and behavior, coordinating with the document model and view components to provide real-time terrain sculpting.

## Cross-References
### Incoming
- **WorldBuilderDoc**: Calls `mouseDown`, `mouseMoved`, `mouseUp` during tool interaction
- **WbView**: Provides view-to-document coordinate conversion in `mouseMoved`
- **BrushOptions**: Updates tool parameters via `setHeight`, `setWidth`, `setFeather`
- **DrawObject**: Manages visual feedback through `setBrushFeedbackParms` and `setFeedbackPos`

### Outgoing
- **WorldHeightMapEdit**: Modifies terrain data via `duplicate`, `getHeight`, `setHeight`
- **WBDocUndoable**: Creates undo commands in `mouseUp`
- **CMainFrame**: Controls UI state in `activate`

## Design Patterns
- **Command Pattern**: Encapsulates brush operations in `WBDocUndoable` for undo/redo support
- **Memento Pattern**: Uses heightmap copies (`m_htMapEditCopy`, `m_htMapFeatherCopy`) to track state changes
- **Observer Pattern**: Notifies `BrushOptions` of parameter changes to keep UI in sync

*Not inferable*: Specific blend factor calculation strategies (square/round)
