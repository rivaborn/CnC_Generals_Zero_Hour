# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwmouse.h - Enhanced Analysis

## Architectural Role
This file defines the core mouse management system for the SAGE engine, bridging OS-level input handling with game-specific cursor rendering. It abstracts mouse operations (capture, visibility, coordinate conversion) to support both in-game and UI contexts.

## Cross-References
### Incoming
- UI systems (e.g., menu navigation, button interactions)
- Input handling subsystems (e.g., event processing loops)
- Rendering pipeline (for cursor drawing/erasing)

### Outgoing
- Windows API (`InterlockedIncrement`, `InterlockedDecrement`)
- `Surface`/`BSurface` classes (for cursor rendering)
- `ShapeSet` (for cursor imagery)

## Design Patterns
- **Singleton-like**: Implied by "only one object" comment (though not enforced).
- **State Pattern**: Mouse visibility/capture states managed via flags (`MouseState`, `IsCaptured`).
- **Pimpl-like**: `BSurface` forward declaration suggests separation of rendering concerns.
