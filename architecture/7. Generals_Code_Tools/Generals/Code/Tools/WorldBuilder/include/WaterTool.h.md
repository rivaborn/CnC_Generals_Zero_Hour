# Generals/Code/Tools/WorldBuilder/include/WaterTool.h

## Purpose
Defines the `WaterTool` class for adding/selecting water polygons in the WorldBuilder editor.

## Responsibilities
- Manages water polygon creation/selection via mouse input
- Handles tool activation/deactivation and cursor updates
- Adjusts water polygon spacing and fills areas with water

## Key Types
- **WaterTool (Class)**: Tool for water polygon operations in WorldBuilder
- **WorldHeightMapEdit (Class)**: External class for heightmap edits (forward declared)
- **MapObject (Class)**: External class for map objects (forward declared)
- **PolygonTrigger (Class)**: External class for polygon triggers (forward declared)
- **MovePolygonUndoable (Class)**: External class for undoable polygon moves (forward declared)

## Key Functions
### WaterTool::mouseDown
- Purpose: Handles mouse down event for water tool.
- Calls: `fillTheArea`

### WaterTool::mouseMoved
- Purpose: Handles mouse movement for water tool.
- Calls: None

### WaterTool::mouseUp
- Purpose: Handles mouse up event for water tool.
- Calls: None

### WaterTool::activate
- Purpose: Activates the water tool.
- Calls: None

### WaterTool::deactivate
- Purpose: Deactivates the water tool.
- Calls: None

### WaterTool::fillTheArea
- Purpose: Fills an area with water.
- Calls: `adjustSpacing`

### WaterTool::adjustSpacing
- Purpose: Adjusts spacing for a polygon trigger.
- Calls: None

## Globals
- **m_water_isActive (Bool)**: Tracks if the water tool is active

## Dependencies
- `PolygonTool.h` (inheritance)
- `WorldHeightMapEdit`, `MapObject`, `PolygonTrigger`, `MovePolygonUndo
