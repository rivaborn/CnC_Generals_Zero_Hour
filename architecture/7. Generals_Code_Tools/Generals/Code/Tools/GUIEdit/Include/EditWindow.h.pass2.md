# Generals/Code/Tools/GUIEdit/Include/EditWindow.h - Enhanced Analysis

## Architectural Role
This file defines the core GUI editor window, bridging the tooling layer with the game's rendering and window management systems. It acts as a singleton facade for the editor's visual interface, coordinating input handling, rendering, and interaction with the game's `GameWindow` hierarchy.

## Cross-References
### Incoming
- **GUIEdit Tool**: Likely calls `init`, `draw`, and `mouseEvent` to drive the editor's UI loop.
- **GameClient/Window System**: Uses `GameWindow` for hierarchy traversal (e.g., `drawSeeThruOutlines`).
- **WW3D2 Renderer**: Depends on `Render2DClass` for 2D drawing operations.

### Outgoing
- **Windows API**: Directly interacts via `HWND`, `editProc`, and message handling.
- **WW3D2 Subsystem**: Uses `WW3DAssetManager` and `Render2DClass` for asset and render management.
- **GameClient**: Relies on `Image` and `GameWindow` for UI element representation.

## Design Patterns
- **Singleton**: Enforces single `EditWindow` instance via `TheEditWindow` global.
- **Facade**: Abstracts complex window management (e.g., drag-resize, clipping) behind simple methods.
- **Observer**: Notifies via `notifyWindowDeleted` when `GameWindow` instances are removed.
