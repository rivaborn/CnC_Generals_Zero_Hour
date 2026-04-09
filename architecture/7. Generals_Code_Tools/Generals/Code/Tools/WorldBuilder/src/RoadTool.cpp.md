# Generals/Code/Tools/WorldBuilder/src/RoadTool.cpp

## Purpose
Implements the road placement tool in WorldBuilder, allowing users to create and manipulate road segments.

## Responsibilities
- Handles road segment creation, snapping, and division
- Manages road endpoint selection and movement
- Integrates with undo/redo system for road modifications
- Supports bridge placement as a special road type
- Maintains road connections between map objects

## Key Types
- RoadTool (Class): Main tool class for road operations
- MapObject (Class): Represents map objects (road endpoints)
- Coord3D (Struct): 3D coordinate structure
- RoadOptions (Class): Stores current road tool settings

## Key Functions
### findSegment
- Purpose: Finds the closest road segment to a given point
- Calls: MapObject::getFirstMapObject, ShortestDistancePointToSegment2D

### snap
- Purpose: Snaps a point to existing road endpoints if within snap distance
- Calls: MapObject::getFirstMapObject, Vector2::Set, Vector2::Length

### activate
- Purpose: Shows the road options panel when tool is activated
- Calls: PointerTool::clearSelection, CMainFrame::GetMainFrame, RoadOptions::updateSelection

### mouseDown
- Purpose: Handles mouse down event to create or modify road segments
- Calls: WbView::viewToDocCoords, RoadOptions::isBridge, TheThingFactory->findTemplate, newInstance, AddObjectUndoable, DeleteObjectUndoable

### mouseMoved
- Purpose: Updates road endpoint position during mouse movement
- Calls: WbView::viewToDocCoords, snap, WbView::snapPoint, CWorldBuilderDoc::invalObject

### mouseUp
- Purpose: Cleans up when mouse button is released
- Calls: None

## Globals
- None

## Dependencies
- StdAfx.h, resource.h
- RoadTool.h, CUndoable.h, DrawObject.h, PointerTool.h, MainFrm.h
- WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h
- W3DDevice/GameClient/HeightMap.h
- Common/WellKnownKeys.h, Common/ThingTemplate.h, Common/ThingFactory.h
- GameClient/Line2D.h
