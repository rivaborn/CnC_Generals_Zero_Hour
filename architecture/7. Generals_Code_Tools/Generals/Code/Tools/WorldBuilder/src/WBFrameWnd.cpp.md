# Generals/Code/Tools/WorldBuilder/src/WBFrameWnd.cpp

## Purpose
Implements frame window classes for WorldBuilder, handling UI layout and window management.

## Responsibilities
- Manages 2D and 3D frame windows
- Handles window positioning and persistence
- Implements toolbar creation and docking
- Manages window size presets for 3D view

## Key Types
- CWBFrameWnd (Class): Base frame window for 2D view
- CWB3dFrameWnd (Class): Frame window for 3D view with size presets

## Key Functions
### CWBFrameWnd::LoadFrame
- Purpose: Loads frame and initializes 2D window layout
- Calls: CFrameWnd::LoadFrame, m_cellSizeToolBar.Create, m_cellSizeToolBar.SetupSlider, DockControlBar

### CWBFrameWnd::OnMove
- Purpose: Saves window position when moved
- Calls: CFrameWnd::OnMove, AfxGetApp()->WriteProfileInt

### CWB3dFrameWnd::LoadFrame
- Purpose: Loads frame and initializes 3D window layout
- Calls: CMainFrame::LoadFrame

### CWB3dFrameWnd::OnMove
- Purpose: Saves 3D window position when moved
- Calls: CFrameWnd::OnMove, AfxGetApp()->WriteProfileInt

### CWB3dFrameWnd::OnWindowPreview1024x768/640x480/800x600
- Purpose: Sets 3D view to specified resolution preset
- Calls: AfxGetApp()->WriteProfileInt, adjustWindowSize

## Globals
- None

## Dependencies
- stdafx.h, worldbuilder.h, MainFrm.h, WBFrameWnd.h,
