# Generals/Code/Tools/Babylon/ExportDlg.cpp

## Purpose
Handles the export dialog UI for localization data in the Babylon tool.

## Responsibilities
- Manages language selection and export options
- Validates and constructs export filenames
- Populates language combo box with available languages
- Handles dialog button states based on selections

## Key Types
- CExportDlg (Class): Dialog class for export settings
- LANGINFO (Struct): Not inferable (external type)
- TR_FILTER (Enum): Not inferable (external type)

## Key Functions
### CExportDlg::OnOK
- Purpose: Validates and processes export settings when OK is clicked
- Calls: GetDlgItem, GetWindowText, _getcwd, strcat, strchr

### CExportDlg::OnInitDialog
- Purpose: Initializes the dialog and populates language combo box
- Calls: GetDlgItem, SetItemDataPtr, InsertString, SetCurSel, SetCheck, SetLimitText

### CExportDlg::OnSelchangeCombolang
- Purpose: Handles language selection changes in combo box
- Calls: GetDlgItem, GetCurSel, GetItemDataPtr, EnableWindow, SetWindowText

## Globals
- max_index (int): Tracks the number of language entries in combo box

## Dependencies
- stdafx.h, noxstring.h, ExportDlg.h, direct.h
- CDialog, CComboBox, CEdit, CButton (MFC classes)
- GetLangInfo, CurrentLanguage (external functions/variables)
- LANGID_UNKNOWN, LANGID_US (external constants)
