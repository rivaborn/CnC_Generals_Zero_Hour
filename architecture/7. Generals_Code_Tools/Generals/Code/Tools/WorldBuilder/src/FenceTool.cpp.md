# Generals/Code/Tools/WorldBuilder/src/FenceTool.cpp

## Purpose
Implements a fence placement tool for the WorldBuilder editor, allowing users to place fences with adjustable spacing and offset.

## Responsibilities
- Manages fence object placement and alignment
- Handles mouse input for fence drawing
- Updates fence object positions dynamically
- Integrates with undo/redo system
- Displays preview objects during interaction

## Key Types
- MAX_OBJECTS (Enum): Maximum number of fence objects allowed (200)

## Key Functions
### FenceTool::updateMapObjectList
- Purpose: Updates the list of fence objects based on current mouse position and spacing
- Calls: ObjectOptions::duplicateCurMapObjectForPlace, WbView3d::removeFenceListObjects, WbView3d::updateFenceListObjects

### FenceTool::mouseDown
- Purpose: Initializes fence placement when mouse button is pressed
- Calls: WbView::viewToDocCoords, WbView::snapPoint, ObjectOptions::duplicateCurMapObjectForPlace, mouseMoved

### FenceTool::mouseMoved
- Purpose: Handles fence preview and updates during mouse movement
- Calls: WbView::viewToDocCoords, WbView::snapPoint, WbView3d::setObjTracking, updateMapObjectList

### FenceTool::mouseUp
- Purpose: Finalizes fence placement when mouse button is released
- Calls: WbView::viewToDocCoords, WbView::snapPoint, updateMapObjectList, WbView3d::removeFenceListObjects, CWorldBuilderDoc::AddAndDoUndoable

## Globals
- None

## Dependencies
- StdAfx.h, resource.h, FenceTool.h, CUndoable.h, DrawObject.h, MainFrm.h, WbView3d.h, WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h, Common/WellKnownKeys.h
- CWorldBuilderDoc, WbView3d, MapObject, ObjectOptions, FenceOptions, AddObjectUndoable, Tool, Coord3D, CPoint, TTrackingMode
