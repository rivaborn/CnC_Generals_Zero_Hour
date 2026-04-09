# Generals/Code/Tools/WorldBuilder/include/MainFrm.h - Enhanced Analysis

## Architectural Role
This file defines the central UI controller for WorldBuilder, orchestrating tool-specific option panels and managing the main application window. It bridges the MFC framework with custom tooling components, serving as the primary entry point for user interaction in the level editing environment.

## Cross-References
### Incoming
- **WorldBuilder UI modules**: Toolbar, status bar, and option panels (e.g., `BrushOptions`, `TerrainMaterial`) likely instantiate or register with `CMainFrame`.
- **WorldBuilder core**: Map editing commands and camera systems call `handleCameraChange` and `OnTimer` for view synchronization and autosave.

### Outgoing
- **MFC framework**: Uses `CFrameWnd`, `CToolBar`, and message handlers for window management.
- **Tool-specific panels**: Hosts and coordinates `BrushOptions`, `ObjectOptions`, etc., via composition.
- **Autosave system**: Likely triggers `OnTimer` callbacks into a persistence layer (not shown in header).

## Design Patterns
- **Composite**: `CMainFrame` aggregates multiple tool option panels (e.g., `BrushOptions`, `LightOptions`) as child components, delegating functionality while maintaining control over layout and visibility.
- **Singleton**: Provides global access via `TheMainFrame` for tool-wide state management (e.g., autosave flags).
- **Observer**: `OnTimer` and `handleCameraChange` suggest event-driven updates, though concrete observers are not visible in the header.
