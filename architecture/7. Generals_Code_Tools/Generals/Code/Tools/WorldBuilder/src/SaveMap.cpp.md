# Generals/Code/Tools/WorldBuilder/src/SaveMap.cpp

## Purpose
Handles the map saving dialog in WorldBuilder, allowing users to select save locations and filenames.

## Responsibilities
- Manages UI for map saving (system/user directories)
- Populates list of existing maps
- Handles file path construction and validation
- Processes user input for save operations

## Key Types
- SaveMap (Class): Dialog class for map saving functionality
- TSaveMapInfo (Struct): Contains save operation parameters (filename, directory preference, etc.)

## Key Functions
### SaveMap::OnOK
- Purpose: Validates and processes save operation when OK is clicked
- Calls: GetWindowText, CFile::GetStatus, AfxMessageBox

### SaveMap::populateMapListbox
- Purpose: Populates the map listbox with existing maps from selected directory
- Calls: FindFirstFile, FindNextFile, CFile::GetStatus, AddString, SetWindowText

### SaveMap::OnSelchangeSaveList
- Purpose: Updates edit control when a map is selected from the list
- Calls: GetCurSel, GetText, SetWindowText

## Globals
- None

## Dependencies
- MFC classes (CDialog, CListBox, CEdit, CButton)
- Common/GlobalData.h (TheGlobalData)
- Windows API (FindFirstFile, FindNextFile)
- Resource IDs (IDC_BROWSE, IDC_SYSTEMMAPS, etc.)
