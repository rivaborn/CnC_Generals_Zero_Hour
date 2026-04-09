# Generals/Code/Tools/WorldBuilder/include/ExportScriptsOptions.h

## Purpose
Header file for the ExportScriptsOptions dialog class, used in WorldBuilder to configure script export options.

## Responsibilities
- Define the ExportScriptsOptions dialog class
- Declare member variables for script export flags
- Declare getter methods for export options
- Declare message handlers for dialog events

## Key Types
- ExportScriptsOptions (Class): Dialog class for script export options
- (anonymous enum) (Enum): Contains IDD enum value
- IDD (Enum): Dialog resource ID

## Key Functions
### ExportScriptsOptions/DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### ExportScriptsOptions/getDoUnits
- Purpose: Returns whether to export unit scripts
- Calls: None

### ExportScriptsOptions/getDoWaypoints
- Purpose: Returns whether to export waypoint scripts
- Calls: None

### ExportScriptsOptions/getDoTriggers
- Purpose: Returns whether to export trigger scripts
- Calls: None

### ExportScriptsOptions/getDoAllScripts
- Purpose: Returns whether to export all scripts
- Calls: None

### ExportScriptsOptions/OnOK
- Purpose: Handles dialog OK button click
- Calls: Not inferable

### ExportScriptsOptions/OnInitDialog
- Purpose: Initializes dialog controls
- Calls: Not inferable

## Globals
- m_units (Bool): Flag for unit script export
- m_waypoints (Bool): Flag for waypoint script export
- m_triggers (Bool): Flag for trigger script export
- m_allScripts (Bool): Flag for all scripts export

## Dependencies
- CDialog (MFC class)
- CWnd (MFC class)
- CDataExchange (MFC class)
- Bool (custom type)
-
