# Generals/Code/Tools/WorldBuilder/src/WBFrameWnd.cpp - Enhanced Analysis

## Architectural Role
This file implements the main frame window classes for WorldBuilder, bridging MFC's window management with the editor's specific UI requirements. It handles persistence of window state and integrates with the toolbar system.

## Cross-References
### Incoming
- `CMainFrame::GetMainFrame()` (from MainFrm.h)
- `WHeightMapEdit` and `WbView3d` (via includes, though not directly referenced in shown code)
- `CCreateContext` (MFC framework)

### Outgoing
- `CFrameWnd` and `CMainFrame` (MFC base classes)
- `AfxGetApp()` (MFC application singleton)
- `m_cellSizeToolBar` (custom toolbar class)

## Design Patterns
- **MVC**: The frame windows act as controllers for the editor's views (2D/3D)
- **Template Method**: Overrides `LoadFrame` to customize MFC's default behavior
- **Observer**: Uses MFC's message map for event handling (e.g., `ON_WM_MOVE`)

*Not inferable*: No clear use of Factory, Strategy, or Decorator patterns in shown code.
