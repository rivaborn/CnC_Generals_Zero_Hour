# Generals/Code/Tools/WorldBuilder/include/SaveMap.h

## Purpose
Header file for the SaveMap dialog class used in WorldBuilder to handle map saving functionality.

## Responsibilities
- Defines the SaveMap dialog class and its data structure
- Manages map save/load UI interactions
- Handles system/user map directory switching
- Provides browse functionality for custom save locations

## Key Types
- TSaveMapInfo (struct): Holds filename, browse flag, and system directory flag
- SaveMap (Class): Dialog class for map save operations
- IDD (Enum): Dialog resource ID

## Key Functions
### SaveMap::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### SaveMap::populateMapListbox
- Purpose: Populates the map listbox with system or user maps
- Calls: Not inferable

### SaveMap::OnOK
- Purpose: Handles OK button click to save the selected map
- Calls: Not inferable

### SaveMap::OnBrowse
- Purpose: Opens file browser for custom save location
- Calls: Not inferable

### SaveMap::OnSystemMaps
- Purpose: Switches to system maps directory
- Calls: Not inferable

### SaveMap::OnUserMaps
- Purpose: Switches to user maps directory
- Calls: Not inferable

### SaveMap::OnSelchangeSaveList
- Purpose: Handles selection change in the save list
- Calls: Not inferable

### SaveMap::OnInitDialog
- Purpose: Initializes the dialog controls
- Calls: Not inferable

## Globals
- MAP_OPENSAVE_PANEL_SECTION (const char*): Configuration section name

## Dependencies
- CDialog, CString, CWnd, Bool (MFC/Windows types
