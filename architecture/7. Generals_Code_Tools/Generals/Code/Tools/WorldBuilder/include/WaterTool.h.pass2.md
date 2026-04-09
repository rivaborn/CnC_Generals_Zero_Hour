# Generals/Code/Tools/WorldBuilder/include/WaterTool.h - Enhanced Analysis

## Architectural Role
This file defines the `WaterTool` class, a specialized tool in the WorldBuilder editor's tool system. It extends the `PolygonTool` base class to handle water polygon operations, integrating with the editor's undo/redo system and map object management.

## Cross-References
### Incoming
- Likely called by the WorldBuilder's tool manager when the water tool is selected
- May be referenced by undo/redo command handlers for polygon operations

### Outgoing
- Inherits from `PolygonTool`, using its core functionality
- Interacts with `WorldHeightMapEdit` for terrain modifications
- Uses `PolygonTrigger` for polygon boundary management
- Potentially creates `MovePolygonUndoable` actions for undo support

## Design Patterns
- **Template Method**: Overrides virtual methods from `PolygonTool` to customize behavior
- **Observer**: Tool activation/deactivation likely notifies the editor UI
- **Command**: `fillTheArea` and `adjustSpacing` may create undoable commands (inferred from `MovePolygonUndoable` dependency)
