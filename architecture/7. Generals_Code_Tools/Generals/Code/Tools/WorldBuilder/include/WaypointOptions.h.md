# Generals/Code/Tools/WorldBuilder/include/WaypointOptions.h

## Purpose
Header for the WaypointOptions dialog class used in WorldBuilder to manage waypoint properties.

## Responsibilities
- Define the WaypointOptions dialog class and its UI handlers
- Provide static methods for waypoint/polygon selection and naming
- Manage waypoint property updates and validation

## Key Types
- **WaypointOptions (Class)**: Dialog for editing waypoint properties
- **MapObject (Class)**: Reference to map objects (forward declared)
- **PolygonTrigger (Class)**: Reference to polygon triggers (forward declared)
- **MovePolygonUndoable (Class)**: Reference to undoable polygon moves (forward declared)
- **(anonymous enum) (Enum)**: Dialog resource ID
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### WaypointOptions::updateTheUI
- Purpose: Refreshes the UI with current waypoint data
- Calls: Not inferable

### WaypointOptions::changeWaypointLabel
- Purpose: Updates a waypoint label with a new key
- Calls: Not inferable

### WaypointOptions::update
- Purpose: Static method to trigger UI updates
- Calls: Not inferable

### WaypointOptions::getSingleSelectedWaypoint
- Purpose: Returns the currently selected waypoint
- Calls: Not inferable

### WaypointOptions::getSingleSelectedPolygon
- Purpose: Returns the currently selected polygon
- Calls: Not inferable

### WaypointOptions::isUnique
- Purpose: Checks if a waypoint name is unique
- Calls: Not inferable

### WaypointOptions::GenerateUniqueName
- Purpose: Generates a unique name for a waypoint
- Calls: Not inferable

## Globals
- **m_staticThis (WaypointOptions*)**: Static reference to the dialog instance
- **m_up
