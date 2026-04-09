# Generals/Code/Tools/WorldBuilder/src/MainFrm.cpp

## Purpose
Implements the main frame window for the WorldBuilder tool, managing UI layout, toolbars, and application state.

## Responsibilities
- Manages the main application window and its child controls (toolbars, status bar, option panels)
- Handles window positioning, sizing, and state persistence
- Controls brush feedback visibility and auto-save functionality
- Coordinates between different editor panels and views

## Key Types
- CMainFrame (Class): Main application frame window
- LayersList (Class): Layer management panel
- DrawObject (Class): Handles brush feedback rendering

## Key Functions
### OnCreate
- Purpose: Initializes the main frame window and its child controls
- Calls: CFrameWnd::OnCreate, adjustWindowSize, SetWindowPos, Create (for toolbars/panels), LoadToolBar

### OnViewBrushfeedback
- Purpose: Toggles brush feedback visibility
- Calls: DrawObject::enableFeedback, DrawObject::disableFeedback

### OnTimer
- Purpose: Handles auto-save timer events
- Calls: CWorldBuilderDoc::GetActiveDoc, SetCursor, SetMessageText, CWorldBuilderDoc::autoSave

### showOptionsDialog
- Purpose: Shows/hides different option panels based on dialog ID
- Calls: SetWindowPos, ShowWindow

## Globals
- indicators (UINT[]): Status bar indicator IDs
- TheMainFrame (CMainFrame*): Singleton instance of the main frame

## Dependencies
- MFC framework classes (CFrameWnd, CWnd, CToolBar, CStatusBar)
- WorldBuilder-specific classes (CWorldBuilderDoc, WbView3d, LayersList)
- Common utilities (GlobalData, DrawObject)
- Resource IDs (IDR_MAINFRAME, IDD_* dialogs)
