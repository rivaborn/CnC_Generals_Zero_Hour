# Generals/Code/Tools/WorldBuilder/src/FeatherTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the feather tool in WorldBuilder, a heightmap editing utility that enables terrain smoothing via blending operations. It bridges the UI layer (mouse input handling) with the core heightmap data structure, demonstrating the editor's tool-based architecture where each tool encapsulates its own state and behavior.

## Cross-References
### Incoming
- **Tool Framework**: Called by the WorldBuilder tool dispatch system when the feather tool is selected.
- **UI System**: `CMainFrame` invokes `activate()` to display tool-specific options.
- **Document System**: `CWorldBuilderDoc` provides heightmap data and handles undo/redo operations.

### Outgoing
- **Tool Options**: Updates `FeatherOptions` dialog with current tool parameters.
- **Rendering**: Uses `DrawObject` for visual feedback (brush cursor).
- **Heightmap Core**: Interacts with `WorldHeightMapEdit` for data manipulation.
- **Undo System**: Creates `WBDocUndoable` commands for reversible operations.

## Design Patterns
- **Command Pattern**: Encapsulates feather operations in `WBDocUndoable` for undo/redo support.
- **State Pattern**: Tool maintains its own state (feather, rate, radius) and transitions via mouse events.
- **Observer Pattern**: Notifies `FeatherOptions` of parameter changes to keep UI in sync.

*Not inferable*: No explicit use of Factory, Strategy, or Visitor patterns.
