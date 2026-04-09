# Generals/Code/Tools/WorldBuilder/src/ObjectTool.cpp

## Purpose
Handles object placement functionality in the WorldBuilder editor.

## Responsibilities
- Manages mouse interactions for object placement
- Calculates object rotation angles based on mouse movement
- Handles object preview and final placement
- Integrates with undo/redo system for object placement

## Key Types
- HYSTERESIS (Enum): Defines hysteresis threshold for mouse movement detection

## Key Functions
### calcAngle
- Purpose: Calculates rotation angle between two 3D points
- Calls: None

### deactivate
- Purpose: Clears object tracking when tool is deactivated
- Calls: CWorldBuilderDoc::GetActiveDoc(), WbView3d::setObjTracking

### activate
- Purpose: Shows object options panel and initializes tool state
- Calls: CMainFrame::GetMainFrame(), showOptionsDialog, DrawObject::setDoBrushFeedback, CWorldBuilderDoc::GetActiveDoc(), WbView3d::setObjTracking

### mouseDown
- Purpose: Records initial mouse position for object placement
- Calls: WbView::viewToDocCoords

### mouseMoved
- Purpose: Handles object preview during mouse movement
- Calls: WbView::viewToDocCoords, WbView::snapPoint, ObjectOptions::getObjectNamed, ObjectOptions::getCurObjectName, ObjectOptions::getCurObjectHeight, WbView3d::setObjTracking

### mouseUp
- Purpose: Finalizes object placement on mouse release
- Calls: WbView::viewToDocCoords, WbView::snapPoint, ObjectOptions::duplicateCurMapObjectForPlace, ObjectOptions::getCurObjectHeight, AddObjectUndoable constructor, CWorldBuilderDoc::AddAndDoUndoable

## Globals
- None
