# Generals/Code/Tools/WorldBuilder/include/PolygonTool.h - Enhanced Analysis

## Architectural Role
This file defines the PolygonTool class, which is part of WorldBuilder's tool system for creating and editing polygon-based area triggers. It extends the base Tool class to provide specialized functionality for polygon manipulation, integrating with the map editing workflow.

## Cross-References
### Incoming
- **WorldBuilder UI**: Likely calls `activate()`/`deactivate()` to switch tools
- **Map Editor**: Uses `pickPolygon()` for selection logic
- **Undo System**: References `MovePolygonUndoable` for state management

### Outgoing
- **Tool.h**: Inherits core tool behavior
- **PolygonTrigger**: Manages trigger geometry and properties
- **WbView**: Handles view transformations for mouse coordinates

## Design Patterns
- **State Pattern**: Tool activation/deactivation manages state transitions
- **Strategy Pattern**: Overrides base Tool methods for polygon-specific behavior
- **Singleton-like Globals**: Static members track tool state across instances

*Not inferable*: Exact undo/redo integration or cursor management details.
