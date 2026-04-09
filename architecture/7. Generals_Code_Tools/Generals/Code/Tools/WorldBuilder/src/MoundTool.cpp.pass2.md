# Generals/Code/Tools/WorldBuilder/src/MoundTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the terrain editing tools (mound/dig) in WorldBuilder, bridging user input with heightmap modifications. It handles brush-based terrain deformation, undo/redo operations, and real-time feedback visualization.

## Cross-References
### Incoming
- `CMainFrame` (UI framework) calls `activate()` to show options dialog
- `WorldBuilderDoc` (document model) provides heightmap via `GetHeightMap()`
- `DrawObject` (rendering) receives feedback parameters via `setBrushFeedbackParms()`

### Outgoing
- `MoundOptions` (UI panel) for tool parameter synchronization
- `DrawObject` for visual feedback during brush operations
- `WBDocUndoable` for undo/redo functionality
- `WorldHeightMapEdit` for heightmap manipulation

## Design Patterns
- **Command Pattern**: Encapsulates terrain modifications in `WBDocUndoable` for undo/redo
- **Observer Pattern**: Notifies `MoundOptions` of parameter changes
- **Strategy Pattern**: `MoundTool`/`DigTool` subclasses implement different terrain modification behaviors

*Not inferable*: Exact implementation of `calcRoundBlendFactor` blending algorithm.
