# Generals/Code/Tools/WorldBuilder/src/BorderTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the map boundary editing tool in WorldBuilder, bridging user input (mouse events) with the document model (CWorldBuilderDoc). It handles coordinate transformations between view and document spaces, enabling real-time boundary manipulation.

## Cross-References
### Incoming
- **WbView** (via mouse event handlers): Calls `mouseDown`, `mouseMoved`, `mouseUp` during tool interaction.
- **CWorldBuilderDoc**: Manages the document state and boundary data, called by `activate`, `deactivate`, and mouse handlers.

### Outgoing
- **DrawObject**: Controls boundary feedback rendering via `setDoBoundaryFeedback`.
- **CMainFrame**: Manages UI state (options dialog) in `activate`.
- **WbView3d**: Retrieves view-specific settings in `deactivate`.

## Design Patterns
- **Command Pattern**: Encapsulates boundary modification operations (add/change) as methods called by the document.
- **State Pattern**: Tracks tool state (`m_addingNewBorder`, `m_modifyBorderNdx`) to determine behavior during mouse events.
- **Strategy Pattern**: Uses `ModificationType` to dynamically select boundary adjustment logic (up/right/free).

*Not inferable*: No explicit use of Observer or Factory patterns.
