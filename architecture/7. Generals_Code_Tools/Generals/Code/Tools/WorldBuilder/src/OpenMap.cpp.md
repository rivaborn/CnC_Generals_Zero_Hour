# Generals/Code/Tools/WorldBuilder/src/OpenMap.cpp

## Purpose
Handles the UI dialog for opening maps in the WorldBuilder tool.

## Responsibilities
- Manages map browsing between system and user directories
- Populates listbox with available maps
- Handles user selection and validation
- Configures UI based on build type (debug/internal vs release)

## Key Types
- OpenMap (Class): Dialog class for map opening functionality
- TOpenMapInfo (Struct): Holds map operation parameters (filename, browse flag)

## Key Functions
### OpenMap::populateMapListbox
- Purpose: Populates the listbox with maps from specified directory
- Calls: FindFirstFile, FindNextFile, FindClose, CFile::GetStatus

### OpenMap::OnOK
- Purpose: Handles dialog confirmation and sets selected map path
- Calls: GetDlgItem, GetCurSel, GetText

### OpenMap::OnInitDialog
- Purpose: Initializes dialog controls and populates map list
- Calls: SetCheck, ShowWindow, populateMapListbox

## Globals
- None

## Dependencies
- MFC classes (CDialog, CListBox, CButton)
- GlobalData (TheGlobalData)
- Windows API (FindFirstFile, etc.)
- STL (CString)
