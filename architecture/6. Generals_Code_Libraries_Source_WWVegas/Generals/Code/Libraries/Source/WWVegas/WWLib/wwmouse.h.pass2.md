# Generals/Code/Libraries/Source/WWVegas/WWLib/wwmouse.h - Enhanced Analysis

## Architectural Role
This file defines the `WWMouseClass`, which serves as the central mouse input and rendering abstraction for the SAGE engine. It bridges low-level OS mouse events with game-specific cursor rendering, handling both input capture and visual representation across multiple surfaces (main game, sidebars, etc.).

## Cross-References
### Incoming
- UI systems (e.g., menu navigation, button interactions)
- Input handling subsystems (e.g., command processing, unit selection)
- Rendering pipeline (for cursor overlay management)

### Outgoing
- `Surface`/`BSurface` classes (for cursor drawing/erasing)
- `ShapeSet` (for cursor imagery)
- OS-specific mouse APIs (via `xmouse.h`)

## Design Patterns
- **Facade Pattern**: Abstracts OS-specific mouse operations behind a unified interface.
- **State Pattern**: Manages mouse visibility/capture states (`MouseState`, `IsCaptured`).
- **Singleton-like**: Implied by the comment "only one object... will be created" (though not enforced in code).
