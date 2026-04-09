# Generals/Code/Tools/WorldBuilder/include/WBFrameWnd.h - Enhanced Analysis

## Architectural Role
This file defines the core windowing infrastructure for WorldBuilder, bridging MFC's windowing system with the editor's 3D viewport requirements. It serves as the foundation for the editor's UI framework, handling both standard and 3D-specific window behaviors.

## Cross-References
### Incoming
- `WorldBuilder.cpp` (main editor entry point)
- `WB3dView.cpp` (3D viewport implementation)
- `WBToolBar.cpp` (toolbar management)
- `WBDocument.cpp` (editor document handling)

### Outgoing
- MFC framework classes (`CFrameWnd`, `CMainFrame`)
- `CellSizeToolBar` (internal toolbar class)
- Windows API for window management

## Design Patterns
- **Decorator Pattern**: Extends MFC's `CFrameWnd` and `CMainFrame` to add editor-specific behavior without modifying base classes.
- **Command Pattern**: Preview mode commands (`OnWindowPreview*`) encapsulate window dimension changes as self-contained operations.
- **Observer Pattern**: `OnUpdateWindowPreview*` methods implement UI state updates in response to command UI state queries.
