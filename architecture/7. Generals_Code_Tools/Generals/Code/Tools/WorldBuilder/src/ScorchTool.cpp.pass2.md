# Generals/Code/Tools/WorldBuilder/src/ScorchTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the scorch mark placement tool in WorldBuilder, bridging the UI layer with the map object system. It handles user input for scorch creation/selection and integrates with the undo/redo framework.

## Cross-References
### Incoming
- **WorldBuilderView**: Calls tool methods during mouse events
- **MainFrm**: Activates/deactivates the tool via UI commands

### Outgoing
- **MapObject**: Queries and modifies scorch marks
- **ScorchOptions**: Syncs tool settings with UI
- **AddObjectUndoable**: Manages undo/redo operations
- **DrawObject**: Controls brush feedback rendering

## Design Patterns
- **Command Pattern**: Encapsulates scorch operations (placement/selection) as discrete actions
- **Observer Pattern**: Updates UI (ScorchOptions) when tool state changes
- **Factory Method**: Uses `newInstance` for MapObject creation (inferred from first-pass)

*Not inferable*: No clear Strategy or Decorator patterns visible in this snippet.
