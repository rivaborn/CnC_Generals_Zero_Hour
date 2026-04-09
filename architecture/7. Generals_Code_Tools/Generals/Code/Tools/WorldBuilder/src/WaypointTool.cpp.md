# Generals/Code/Tools/WorldBuilder/src/WaypointTool.cpp

## Purpose
Handles waypoint creation, selection, and linking in the WorldBuilder tool.

## Responsibilities
- Manages waypoint tool activation/deactivation
- Handles mouse interactions for waypoint manipulation
- Creates new waypoints and links them
- Updates waypoint options UI

## Key Types
- WaypointTool (Class): Main tool class for waypoint operations
- WaypointOptions (Class): Not inferable (used for UI updates)
- MapObject (Class): Represents map objects including waypoints
- AddObjectUndoable (Class): Undoable action for object addition

## Key Functions
### pickWaypoint
- Purpose: Finds the closest waypoint to a given coordinate
- Calls: MapObject::getFirstMapObject, MapObject::getNext, MapObject::isWaypoint, MapObject::getLocation

### mouseDown
- Purpose: Handles left mouse button down for waypoint selection/creation
- Calls: pickWaypoint, newInstance, MapObject::setSelected, MapObject::setIsWaypoint, MapObject::setWaypointID, MapObject::setWaypointName, MapObject::getProperties, AddObjectUndoable constructor, CWorldBuilderDoc::AddAndDoUndoable, WaypointOptions::update

### mouseMoved
- Purpose: Handles mouse movement for waypoint dragging visualization
- Calls: pickWaypoint, DrawObject::setWaypointDragFeedback, WbView::Invalidate

### mouseUp
- Purpose: Handles left mouse button up for waypoint placement/linking
- Calls: pickWaypoint, PointerTool::clearSelection, newInstance, MapObject::setSelected, CWorldBuilderDoc::waypointLinkExists, CWorldBuilderDoc::removeWaypointLink, CWorldBuilderDoc::addWaypointLink, CWorldBuilderDoc::getWaypointByID, CWorldBuilderDoc::updateLinkedWaypointLabels, WaypointOptions::update

## Globals
- m_isActive (Bool): Tracks if the waypoint tool is active

## Dependencies
- StdAfx.h, resource.h, WaypointTool.h, PointerTool.h, CUndoable.h, TerrainMaterial.h, WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h, MainFrm.h, DrawObject.h, Common/WellKnownKeys.h
- MapObject, Coord3D, AsciiString, Int, TTrackingMode, CPoint, WbView, CWorldBuilderDoc, AddObjectUndoable, REF_PTR_RELEASE
