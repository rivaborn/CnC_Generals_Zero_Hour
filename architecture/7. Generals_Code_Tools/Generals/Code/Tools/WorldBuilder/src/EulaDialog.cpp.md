# Generals/Code/Tools/WorldBuilder/src/EulaDialog.cpp

## Purpose
Handles the End User License Agreement (EULA) dialog in the WorldBuilder tool.

## Responsibilities
- Displays EULA text from string resources
- Manages dialog initialization and message mapping
- Provides basic MFC dialog functionality

## Key Types
- EulaDialog (class): MFC dialog class for EULA display

## Key Functions
### EulaDialog::EulaDialog
- Purpose: Constructor for EULA dialog
- Calls: CDialog constructor

### EulaDialog::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: CDialog::DoDataExchange

### EulaDialog::OnInitDialog
- Purpose: Initializes the dialog and loads EULA text from resources
- Calls: CDialog::OnInitDialog, CString::LoadString, CWnd::SetWindowText

## Globals
- THIS_FILE (char[]): Debug file tracking variable

## Dependencies
- stdafx.h, worldbuilder.h, euladialog.h
- MFC classes: CDialog, CWnd, CString
- Resource IDs: IDS_EULA_AGREEMENT1-5, IDD (dialog template)
