# Generals/Code/Tools/WorldBuilder/include/HandScrollTool.h - Enhanced Analysis

## Architectural Role
This file defines the `HandScrollTool` class, a concrete implementation of the `Tool` base class in the WorldBuilder editor. It handles view panning via mouse input, integrating with the editor's tool system and view management.

## Cross-References
### Incoming
- `WorldBuilder` UI framework (calls `activate()`, `mouseDown`, `mouseMoved`, `mouseUp`)
- `ToolManager` (instantiates and manages tool lifecycle)

### Outgoing
- `Tool.h` (inherits from `Tool`)
- `WbView` (modifies view state in `mouseMoved`)
- `CWorldBuilderDoc` (passed as parameter for context)

## Design Patterns
- **Template Method**: Overrides virtual methods from `Tool` base class (e.g., `mouseDown`, `mouseMoved`).
- **State Pattern**: Manages scrolling state (`m_scrolling`, `m_mouseDownTime`) for behavior switching.
- **Hysteresis**: Uses `HYSTERESIS` constant to debounce mouse movement for smoother input.

*Not inferable: No clear use of Observer, Factory, or Strategy patterns.*
