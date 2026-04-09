# Generals/Code/Tools/WorldBuilder/include/OpenMap.h

## Purpose
Header file for the OpenMap dialog class, used to select and open map files in WorldBuilder.

## Responsibilities
- Defines the OpenMap dialog class and its data structure.
- Manages map file selection between system and user directories.
- Handles UI interactions for browsing and selecting maps.

## Key Types
- TOpenMapInfo (struct): Holds filename and browse flag for map selection.
- OpenMap (Class): Dialog class for opening maps.
- IDD (Enum): Dialog resource ID.

## Key Functions
### OpenMap::populateMapListbox
- Purpose: Populates the listbox with map files from the specified directory.
- Calls: Not inferable.

### OpenMap::OnBrowse
- Purpose: Handles the browse button click event.
- Calls: Not inferable.

### OpenMap::OnSystemMaps
- Purpose: Switches to system maps directory.
- Calls: Not inferable.

### OpenMap::OnUserMaps
- Purpose: Switches to user maps directory.
- Calls: Not inferable.

### OpenMap::OnOK
- Purpose: Handles the OK button click event to confirm map selection.
- Calls: Not inferable.

### OpenMap::OnInitDialog
- Purpose: Initializes the dialog and populates the map listbox.
- Calls: Not inferable.

### OpenMap::OnDblclkOpenList
- Purpose: Handles double-click event on the map listbox.
- Calls: Not inferable.

## Globals
- MAP_OPENSAVE_PANEL_SECTION (const char*): Section name for configuration.

## Dependencies
- CString, Bool (MFC/STL types)
- CDialog, CWnd (MFC classes)
- CDataExchange (MFC class)
- DECLARE_MESSAGE_MAP() (MFC macro
