# Generals/Code/Tools/WorldBuilder/include/CUndoable.h - Enhanced Analysis

## Architectural Role
This file defines the undo/redo command pattern implementation for the WorldBuilder tool, serving as the core of its document modification tracking system. It bridges the gap between user actions and the underlying map data structures, enabling non-destructive editing operations.

## Cross-References
### Incoming
- WorldBuilder UI commands (e.g., object placement, terrain editing)
- Document management classes (CWorldBuilderDoc)
- Map editing operations (heightmap, object, polygon modifications)

### Outgoing
- CWorldBuilderDoc methods for applying/reverting changes
- WorldHeightMapEdit for terrain modifications
- MapObject and PolygonTrigger for game entity operations

## Design Patterns
- **Command Pattern**: Encapsulates actions as objects (Undoable hierarchy) to support undo/redo
- **Composite Pattern**: Chains undoable commands via linked list (mNext)
- **Memento Pattern**: Captures and externalizes object state (MoveInfo, DeleteInfo, FlagsInfo) for restoration

*Not inferable*: Specific usage of RefCountClass for memory management.
