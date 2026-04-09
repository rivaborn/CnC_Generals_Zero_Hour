# Generals/Code/Tools/WW3D/max2w3d/SceneSetupDlg.cpp

## Purpose
Implements a dialog for configuring scene export settings in the max2w3d tool.

## Responsibilities
- Manages a modal dialog for LOD and damage model export options
- Handles user input for clone procedures and offset values
- Validates numeric input fields
- Updates internal state based on user selections

## Key Types
- **SceneSetupDlg (Class)**: Dialog controller for scene export settings
- **Interface (Type)**: 3DS Max interface reference (external)

## Key Functions
### SceneSetupDlg::DoModal
- Purpose: Displays the dialog and returns user action result
- Calls: DialogBoxParam, _thunk_dialog_proc

### SceneSetupDlg::DialogProc
- Purpose: Handles Windows messages for the dialog
- Calls: OnInitDialog, OnOK, EndDialog

### SceneSetupDlg::OnInitDialog
- Purpose: Initializes dialog controls with current settings
- Calls: CenterWindow, CheckDlgButton, SetEditInt, SetEditFloat

### SceneSetupDlg::OnOK
- Purpose: Validates and saves user input when OK is clicked
- Calls: ValidateEditFloat, MessageBox, IsDlgButtonChecked, GetEditInt, GetEditFloat

## Globals
- **_thunk_dialog_proc (Function)**: Thunk function for dialog procedure

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `Interface` class (3DS Max interface)
- Windows API (DialogBoxParam, EndDialog, etc.)
- Standard C runtime (sprintf, sscanf)
