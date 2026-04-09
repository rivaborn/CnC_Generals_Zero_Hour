# Generals/Code/Tools/WorldBuilder/src/CellWidth.cpp

## Purpose
Handles the UI dialog for setting cell width in WorldBuilder.

## Responsibilities
- Manages cell width input/output via a combo box
- Initializes and validates the dialog
- Processes OK button click to retrieve user input

## Key Types
- CellWidth (class): Dialog class for cell width configuration

## Key Functions
### CellWidth::CellWidth(int cellWidth, CWnd* pParent)
- Purpose: Constructor initializing cell width and parent window
- Calls: CDialog constructor

### CellWidth::OnOK()
- Purpose: Retrieves cell width value from UI on dialog acceptance
- Calls: GetDlgItem, GetWindowText, atoi, CDialog::OnOK

### CellWidth::OnInitDialog()
- Purpose: Initializes the dialog with the current cell width value
- Calls: CDialog::OnInitDialog, GetDlgItem, SetWindowText

## Globals
- None

## Dependencies
- "stdafx.h", "worldbuilder.h", "CellWidth.h"
- CDialog, CWnd, CString, CDataExchange, BEGIN_MESSAGE_MAP, END_MESSAGE_MAP
