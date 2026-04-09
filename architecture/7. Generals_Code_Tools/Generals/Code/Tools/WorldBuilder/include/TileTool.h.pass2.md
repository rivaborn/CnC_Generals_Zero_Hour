# Generals/Code/Tools/WorldBuilder/include/TileTool.h - Enhanced Analysis

## Architectural Role
This file defines the core tool classes for texture tiling in WorldBuilder, extending the base `Tool` class. It bridges the UI input layer with the terrain editing subsystem (`WorldHeightMapEdit`), enabling real-time texture placement during map creation.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls `mouseDown`, `mouseUp`, `mouseMoved` for input handling.
- **Tool Manager**: Invokes `activate()` during tool switching.
- **BigTileTool-specific UI**: Calls `setWidth()` for brush size adjustments.

### Outgoing
- **WorldHeightMapEdit**: Uses `m_htMapEditCopy` for terrain modifications.
- **Tool Base Class**: Inherits and overrides virtual methods from `Tool.h`.

## Design Patterns
- **Template Method**: Overrides `mouseDown`/`mouseUp` in derived classes while keeping core logic in base.
- **Strategy**: Encapsulates different tile behaviors (e.g., `BigTileTool`) behind a common interface.
- **Observer**: Reacts to mouse events to modify terrain state (implicit in `Tool` hierarchy).
