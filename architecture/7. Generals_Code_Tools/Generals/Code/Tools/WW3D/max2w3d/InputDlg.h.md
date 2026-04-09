# Generals/Code/Tools/WW3D/max2w3d/InputDlg.h

## Purpose
Defines a generic input dialog class for MAXScript integration in the max2w3d tool.

## Responsibilities
- Provides a modal input dialog with caption, label, and value fields
- Manages dialog procedure and message handling
- Stores user input in internal buffers
- Handles MAXScript callback integration

## Key Types
- InputDlg (Class): Generic input dialog wrapper for MAXScript
- (anonymous enum) (Enum): Dialog resource ID container
- IDD (Enum): Dialog resource identifier

## Key Functions
### InputDlg::DoModal
- Purpose: Displays the modal input dialog and returns user action result
- Calls: DialogProc, OnInitDialog, OnOK

### InputDlg::DialogProc
- Purpose: Handles Windows messages for the dialog
- Calls: OnInitDialog, OnOK

### InputDlg::OnInitDialog
- Purpose: Initializes dialog controls with stored values
- Calls: None

### InputDlg::OnOK
- Purpose: Processes OK button click and retrieves user input
- Calls: None

## Globals
- None

## Dependencies
- dllmain.h
- resource.h
- Windows API (HWND, WPARAM, LPARAM, BOOL CALLBACK)
- MAXScript integration symbols (via _thunk_dialog_proc)
