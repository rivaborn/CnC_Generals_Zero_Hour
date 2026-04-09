# Generals/Code/Tools/WorldBuilder/src/PointerTool.cpp

## Purpose
Implements the PointerTool class for the WorldBuilder editor, handling object selection, manipulation, and waypoint management.

## Responsibilities
- Manages object selection and manipulation (move/rotate)
- Handles waypoint selection and path-based waypoint picking
- Implements drag selection for multiple objects
- Manages polygon trigger interactions
- Controls cursor behavior based on tool state

## Key Types
- **PointerTool (Class)**: Main tool class for object manipulation
- **ModifyObjectUndoable (Class)**: Undoable action for object modifications
- **MapObject (Class)**: Represents objects in the world

## Key Functions
### `pickAllWaypointsInPath`
- Purpose: Selects/deselects all waypoints connected to a source waypoint via links
- Calls: `helper_pickAllWaypointsInPath`

### `helper_pickAllWaypointsInPath`
- Purpose: Recursively finds all waypoints connected to a source waypoint
- Calls: None (recursive)

### `mouseDown`
- Purpose: Handles mouse down events for object selection/manipulation
- Calls: `allowPick`, `pickAllWaypointsInPath`, `poly_pickOnMouseDown`

### `mouseMoved`
- Purpose: Handles mouse movement for object dragging/rotating
- Calls: `allowPick`, `invalObjectInView`

### `mouseUp`
- Purpose: Handles mouse up events for finalizing actions
- Calls: `doRectFeedback`, `invalObject`

## Globals
- **m_modifyUndoable (ModifyObjectUndoable*)**: Tracks object modifications for undo
- **m_curObject (MapObject*)**: Currently selected object
- **m_rotateCursor (HCURSOR)**: Custom rotate cursor
- **m_moveCursor (HCURSOR)**: Custom move cursor

## Dependencies
- `StdAfx.h`, `resource.h`, `PointerTool.h`, `CUndoable.h`
- `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`
- `WorldBuilderView.h`, `GameLogic/SidesList.h`
- `Common/ThingSort.h`, `Common/ThingTemplate.h`
- `GameLogic/PolygonTrigger.h`, `WBView3D.h`, `ObjectTool.h`
