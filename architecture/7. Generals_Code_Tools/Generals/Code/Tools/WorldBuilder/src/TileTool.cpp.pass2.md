# Generals/Code/Tools/WorldBuilder/src/TileTool.cpp - Enhanced Analysis

## Architectural Role
This file implements terrain texture painting tools in WorldBuilder, bridging user input with heightmap modification. It handles brush-based texture application, undo/redo integration, and visual feedback, serving as a core component of the level editing pipeline.

## Cross-References
### Incoming
- **BrushTool.h**: Likely uses TileTool as a base class or related tool
- **MainFrm.h**: Calls `showOptionsDialog()` to display terrain material UI
- **WorldBuilderDoc.h**: Manages document state and undo operations

### Outgoing
- **DrawObject.h**: For brush feedback visualization
- **TerrainMaterial.h**: For texture selection and painting options
- **WHeightMapEdit.h**: For heightmap modification and optimization

## Design Patterns
- **Command Pattern**: Encapsulates terrain modifications in `WBDocUndoable` for undo/redo
- **State Pattern**: Different mouse tracking modes (`TRACK_L`, `TRACK_R`) alter behavior
- **Observer Pattern**: Updates UI via `UpdateWindow()` after modifications

*Not inferable*: Exact brush feedback mechanism or tile optimization strategy.
