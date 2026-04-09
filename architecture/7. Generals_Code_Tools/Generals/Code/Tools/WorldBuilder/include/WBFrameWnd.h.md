# Generals/Code/Tools/WorldBuilder/include/WBFrameWnd.h

## Purpose
Defines base and 3D frame window classes for the WorldBuilder tool, extending MFC's CFrameWnd and CMainFrame.

## Responsibilities
- Provides custom frame window behavior for WorldBuilder
- Manages window resizing and preview modes
- Handles toolbar integration (CellSizeToolBar)
- Implements message handling for window events

## Key Types
- **CWBFrameWnd (Class)**: Base frame window class for WorldBuilder
- **CWB3dFrameWnd (Class)**: 3D frame window class with preview modes
- **CellSizeToolBar (Type)**: Toolbar member for CWBFrameWnd (not defined here)

## Key Functions
### CWBFrameWnd::LoadFrame
- Purpose: Loads frame resources with custom style
- Calls: None visible

### CWBFrameWnd::OnMove
- Purpose: Handles window move events
- Calls: None visible

### CWB3dFrameWnd::LoadFrame
- Purpose: Loads 3D frame resources with custom style
- Calls: None visible

### CWB3dFrameWnd::OnMove
- Purpose: Handles 3D window move events
- Calls: None visible

### CWB3dFrameWnd::OnWindowPreview1024x768/640x480/800x600
- Purpose: Sets window preview dimensions
- Calls: None visible

### CWB3dFrameWnd::OnUpdateWindowPreview1024x768/640x480/800x600
- Purpose: Updates UI state for preview modes
- Calls: None visible

### CWB3dFrameWnd::OnPaint
- Purpose: Handles 3D window painting
- C
