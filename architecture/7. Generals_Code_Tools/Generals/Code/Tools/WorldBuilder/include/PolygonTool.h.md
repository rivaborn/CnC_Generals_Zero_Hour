# Generals/Code/Tools/WorldBuilder/include/PolygonTool.h

## Purpose
Defines the PolygonTool class for creating and editing polygon area triggers in WorldBuilder.

## Responsibilities
- Manages polygon selection and editing operations
- Handles mouse interactions for polygon manipulation
- Provides cursor feedback during polygon editing
- Tracks polygon state (active, selected, etc.)

## Key Types
- **PolygonTool (Class)**: Main tool class for polygon operations
- **WorldHeightMapEdit (Class)**: External dependency (not defined here)
- **MapObject (Class)**: External dependency (not defined here)
- **PolygonTrigger (Class)**: External dependency (not defined here)
- **MovePolygonUndoable (Class)**: External dependency (not defined here)

## Key Functions
### PolygonTool::mouseDown
- Purpose: Handles mouse down events for polygon editing
- Calls: poly_pickOnMouseDown, startMouseDown

### PolygonTool::mouseMoved
- Purpose: Handles mouse movement during polygon editing
- Calls: Not inferable

### PolygonTool::mouseUp
- Purpose: Handles mouse up events for polygon editing
- Calls: Not inferable

### PolygonTool::poly_pickPoint
- Purpose: Picks a point on a polygon
- Calls: Not inferable

### PolygonTool::poly_pickPoly
- Purpose: Picks a polygon at a given location
- Calls: Not inferable

## Globals
- **m_poly_isActive (Bool)**: Tracks if polygon tool is active
- **m_poly_curSelectedPolygon (PolygonTrigger*)**: Currently selected polygon
- **m_poly_dragPointNdx (Int)**: Index of dragged point
- **m_poly_isAdding (Bool)**: Tracks if adding points to polygon

## Dependencies
- Key includes: "Tool.h"
- External symbols: WorldHeight
