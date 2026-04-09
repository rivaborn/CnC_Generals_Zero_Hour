# Generals/Code/Tools/WorldBuilder/include/BrushTool.h - Enhanced Analysis

## Architectural Role
This file defines the `BrushTool` class, a concrete implementation of the `Tool` abstract base class in WorldBuilder's terrain editing system. It handles heightmap modifications via brush-based input, integrating with the document-view architecture for real-time terrain manipulation.

## Cross-References
### Incoming
- `WorldBuilderDoc` (likely calls `activate()`, `mouseDown/Up/Moved` for tool activation and input handling)
- Other `Tool`-derived classes (may reference static brush parameters)

### Outgoing
- `WorldHeightMapEdit` (for heightmap modifications)
- `Tool` base class (inherits core tool behavior)

## Design Patterns
- **Template Method**: Overrides `Tool` virtual methods (`mouseDown/Up/Moved`) to define brush-specific behavior.
- **State Pattern**: Tool activation/deactivation manages state transitions (implicit via `activate()`).
- **Singleton-like**: Static brush parameters suggest shared state across tool instances (though not a pure singleton).

*Not inferable*: Exact undo/redo integration or feathering algorithm details.
