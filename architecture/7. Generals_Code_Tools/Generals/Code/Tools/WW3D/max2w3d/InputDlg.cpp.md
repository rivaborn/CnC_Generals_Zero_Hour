# Generals/Code/Tools/WW3D/max2w3d/InputDlg.cpp

## Purpose
Implements a modal input dialog for user text entry in the max2w3d tool.

## Responsibilities
- Manages dialog creation and display
- Handles user input validation
- Updates internal state based on user input
- Provides accessors for dialog content

## Key Types
- InputDlg (Class): Modal input dialog wrapper
- None

## Key Functions
### InputDlg::DoModal
- Purpose: Displays the modal dialog and returns user action result
- Calls: DialogBoxParam, _thunk_dialog_proc

### InputDlg::DialogProc
- Purpose: Handles Windows messages for the dialog
- Calls: OnInitDialog, OnOK, EndDialog

### InputDlg::OnInitDialog
- Purpose: Initializes dialog controls with stored values
- Calls: SetWindowText, GetDlgItem, SendMessage

### InputDlg::OnOK
- Purpose: Validates and retrieves user input when OK is clicked
- Calls: GetDlgItem, GetWindowText

## Globals
- None

## Dependencies
- InputDlg.h
- Windows API (HWND, WPARAM, LPARAM, etc.)
- Dialog resource (IDD, IDC_LABEL, IDC_VALUE, etc.)
- AppInstance (external global)
