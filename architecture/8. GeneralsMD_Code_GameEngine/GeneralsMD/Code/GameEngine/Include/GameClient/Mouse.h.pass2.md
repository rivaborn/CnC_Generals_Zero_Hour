# GeneralsMD/Code/GameEngine/Include/GameClient/Mouse.h - Enhanced Analysis

## Architectural Role
This file defines the core mouse input subsystem interface, bridging hardware input with game UI interactions. It abstracts mouse state management, cursor rendering, and tooltip display, serving as the central point for all mouse-related operations in the SAGE engine.

## Cross-References
### Incoming
- **UI System**: Calls `setCursorTooltip()`, `draw()`, and `isClick()` for cursor/tooltip management
- **Input System**: Uses `update()` to process mouse events
- **Render System**: Leverages `draw()` for cursor rendering (W3D/DX8/software paths)

### Outgoing
- **DisplayString**: Uses `DisplayString` for tooltip/cursor text rendering
- **W3D System**: References W3D model/anim names in `CursorInfo` for 3D cursors
- **INI System**: Calls `parseIni()` to load mouse configuration

## Design Patterns
- **Singleton**: `TheMouse` provides global access to mouse state
- **Strategy**: `RedrawMode` enum enables different cursor rendering backends (W3D/DX8/software)
- **Observer**: Mouse events trigger UI updates via `update()`/`draw()` calls

*Not inferable: Exact event queueing mechanism or force feedback integration details.*
