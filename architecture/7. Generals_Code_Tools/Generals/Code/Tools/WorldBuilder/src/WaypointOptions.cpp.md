# Generals/Code/Tools/WorldBuilder/src/WaypointOptions.cpp

## Purpose
Handles UI for waypoint and polygon trigger editing in WorldBuilder.

## Responsibilities
- Manages waypoint/polygon selection and property editing
- Updates UI based on current selection
- Handles name uniqueness and validation
- Syncs waypoint locations and labels with document

## Key Types
- **WaypointOptions (class)**: Dialog for waypoint/polygon editing
- **MapObject (external)**: Represents map objects (waypoints)
- **PolygonTrigger (external)**: Represents area triggers

## Key Functions
### updateTheUI
- Purpose: Refreshes UI controls based on current selection
- Calls: getSingleSelectedWaypoint, getSingleSelectedPolygon

### OnChangeSelectedWaypoint
- Purpose: Handles waypoint selection from dropdown
- Calls: getSingleSelectedWaypoint, setSelected, setCenterInView

### OnChangeWaypointnameEdit
- Purpose: Updates waypoint/trigger name when edited
- Calls: isUnique, setWaypointName, setTriggerName

### changeWaypointLabel
- Purpose: Updates waypoint path labels
- Calls: getProperties, setAsciiString, updateLinkedWaypointLabels

## Globals
- **m_staticThis (WaypointOptions*)**: Singleton instance pointer

## Dependencies
- MFC (CDialog, CWnd, CComboBox)
- WorldBuilder doc/view classes
- MapObject, PolygonTrigger, Tool
- NameKeyGenerator, LayersList
- WellKnownKeys constants
