# GeneralsMD/Code/GameEngine/Include/GameClient/GameWindow.h - Enhanced Analysis

## Architectural Role
This header defines the core UI windowing system for the SAGE engine, serving as the foundation for all in-game UI elements. It establishes the window hierarchy, event handling, and rendering callbacks that power menus, HUD elements, and moddable UI components.

## Cross-References
### Incoming
- UI-related files (e.g., buttons, sliders) inherit from `GameWindow`
- Game state managers call window system functions for UI updates
- Input system routes mouse/keyboard events to window callbacks

### Outgoing
- Calls into `WinInstanceData` for window-specific data
- Uses `Image` and `Color` for rendering
- Relies on `GameFont` for text display

## Design Patterns
- **Callback Pattern**: Uses function pointers (`GameWinDrawFunc`, etc.) for event handling, enabling flexible UI behavior
- **Composite Pattern**: Window hierarchy (`m_parent`, `m_child`) allows complex UI layouts
- **Strategy Pattern**: Different window types implement their own callbacks while sharing the base `GameWindow` interface

*Not inferable*: Exact memory management strategy for window objects (though `MemoryPoolObject` is used for `ModalWindow`).
