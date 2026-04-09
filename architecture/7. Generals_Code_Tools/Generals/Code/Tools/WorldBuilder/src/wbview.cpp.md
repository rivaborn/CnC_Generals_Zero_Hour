# Generals/Code/Tools/WorldBuilder/src/wbview.cpp

## Purpose
Handles the main view and interaction logic for the WorldBuilder tool, managing map editing, object selection, and UI feedback.

## Responsibilities
- Manages mouse input and view tracking
- Handles object selection and display toggles
- Coordinates with tools and undo system
- Updates status bar with map info
- Manages view settings (grid snapping, labels, etc.)

## Key Types
- WbView (Class): Main view class handling map editing and display
- TTrackingMode (Enum): Tracks mouse button states (TRACK_NONE, TRACK_L, TRACK_R, TRACK_M)
- TPickedStatus (Enum): Object picking states (PICK_NONE, PICK_CENTER, PICK_ARROW)

## Key Functions
### mouseDown
- Purpose: Initiates mouse tracking and tool interaction
- Calls: SetCapture, WbApp()->updateCurTool, WbApp()->getCurTool()->mouseDown

### mouseMove
- Purpose: Handles mouse movement and status updates
- Calls: PeekMessage, WbApp()->getCurTool()->mouseMoved, TheTerrainRenderObject->getHeightMapHeight

### mouseUp
- Purpose: Ends mouse tracking and tool interaction
- Calls: ReleaseCapture, WbApp()->getCurTool()->mouseUp, WbApp()->unlockCurTool

### picked
- Purpose: Determines if a point picks an object
- Calls: None

### OnViewShowObjects
- Purpose: Toggles object visibility
- Calls: None

## Globals
- m_snapToGrid (Bool): Tracks grid snapping preference
- ApplicationHWnd (HWND): Stores the application window handle

## Dependencies
- CUndoable.h, worldbuilder.h, wbview.h, wheightmapedit.h
- Common/Debug.h, Common/ThingTemplate.h
- W3DDevice/GameClient/HeightMap.h
- GlobalLightOptions.h, PlayerListDlg.h, TeamsDialog.h
- MFC classes (CView, CPoint, CString, etc.)
- MapObject, WorldHeightMapEdit, ThingTemplate, Dict classes
