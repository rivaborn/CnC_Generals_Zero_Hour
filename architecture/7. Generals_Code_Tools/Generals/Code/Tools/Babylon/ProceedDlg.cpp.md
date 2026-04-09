# Generals/Code/Tools/Babylon/ProceedDlg.cpp

## Purpose
Implements a modal dialog for user confirmation with Yes/No/Always options.

## Responsibilities
- Displays a message and waits for user input
- Handles button clicks (Yes, No, Always)
- Manages dialog initialization and cleanup

## Key Types
- ProceedDlg (class): Dialog class for user confirmation

## Key Functions
### ProceedDlg::OnYes
- Purpose: Closes dialog with IDYES result
- Calls: EndDialog

### ProceedDlg::OnAlways
- Purpose: Closes dialog with IDALWAYS result
- Calls: EndDialog

### ProceedDlg::OnNo
- Purpose: Closes dialog with IDNO result
- Calls: EndDialog

### ProceedDlg::OnClose
- Purpose: Handles window close event
- Calls: EndDialog, CDialog::OnClose

### ProceedDlg::OnInitDialog
- Purpose: Initializes dialog controls
- Calls: CDialog::OnInitDialog, SetDlgItemText

## Globals
- THIS_FILE (char[]): Debug file identifier

## Dependencies
- stdafx.h, noxstring.h, ProceedDlg.h
- MFC classes: CDialog, CWnd, CDataExchange
- Windows API: EndDialog
