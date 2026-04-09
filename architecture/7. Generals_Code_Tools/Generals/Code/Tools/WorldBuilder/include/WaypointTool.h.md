# Generals/Code/Tools/WorldBuilder/include/WaypointTool.h

## Purpose
Defines the WaypointTool class for selecting and manipulating waypoints in WorldBuilder.

## Responsibilities
- Handles waypoint selection and manipulation
- Manages mouse input for waypoint operations
- Tracks active state of the tool
- Interacts with MapObject and WorldHeightMapEdit

## Key Types
- WaypointTool (Class): Tool for waypoint operations in WorldBuilder
- WorldHeightMapEdit (Class): Not inferable (forward declared)
- MapObject (Class): Not inferable (forward declared)

## Key Functions
### WaypointTool::pickWaypoint
- Purpose: Selects a waypoint at the given location
- Calls: Not inferable

### WaypointTool::mouseDown
- Purpose: Handles mouse down event for waypoint selection
- Calls: Not inferable

### WaypointTool::mouseMoved
- Purpose: Handles mouse movement during waypoint operations
- Calls: Not inferable

### WaypointTool::mouseUp
- Purpose: Handles mouse up event for waypoint operations
- Calls: Not inferable

### WaypointTool::activate
- Purpose: Activates the waypoint tool
- Calls: Not inferable

### WaypointTool::deactivate
- Purpose: Deactivates the waypoint tool
- Calls: Not inferable

## Globals
- m_isActive (Bool): Tracks whether the waypoint tool is active

## Dependencies
- Tool.h (base class)
- Forward declarations: WorldHeightMapEdit, MapObject
