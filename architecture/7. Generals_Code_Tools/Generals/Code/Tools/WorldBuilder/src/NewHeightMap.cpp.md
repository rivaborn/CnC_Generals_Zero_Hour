# Generals/Code/Tools/WorldBuilder/src/NewHeightMap.cpp

## Purpose
Handles the UI dialog for creating or modifying heightmaps in the WorldBuilder tool.

## Responsibilities
- Displays and manages input fields for heightmap dimensions and settings
- Handles anchor point selection for heightmap positioning
- Validates and stores user input when dialog is confirmed
- Initializes dialog controls based on existing heightmap data

## Key Types
- CNewHeightMap (Class): Dialog class for heightmap configuration
- TNewHeightInfo (Struct): Contains heightmap parameters (dimensions, anchors, etc.)

## Key Functions
### CNewHeightMap::OnInitDialog
- Purpose: Initializes dialog controls with existing heightmap data
- Calls: CDialog::OnInitDialog, GetDlgItem, SetWindowText, ShowWindow

### CNewHeightMap::doAnchorButton
- Purpose: Handles anchor point button clicks and updates anchor state
- Calls: GetDlgItem, SetCheck

### CNewHeightMap::OnOK
- Purpose: Reads user input and updates heightmap parameters
- Calls: GetDlgItem, GetWindowText, atoi, CDialog::OnOK

### CNewHeightMap::OnCommand
- Purpose: Handles button click events, particularly anchor buttons
- Calls: doAnchorButton, CDialog::OnCommand

## Globals
- None

## Dependencies
- MFC classes (CDialog, CWnd, CButton, CString)
- WorldBuilder-specific headers (worldbuilder.h, NewHeightMap.h)
- Standard C++ types (Int, Bool)
