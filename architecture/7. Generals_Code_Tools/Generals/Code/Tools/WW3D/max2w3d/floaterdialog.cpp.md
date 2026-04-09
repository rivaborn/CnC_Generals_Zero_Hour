# Generals/Code/Tools/WW3D/max2w3d/floaterdialog.cpp

## Purpose
Implements a floating dialog window system for the Max2W3d tool, managing child dialogs within a parent floater window.

## Responsibilities
- Manages creation and destruction of floating dialog windows
- Handles child dialog embedding and sizing
- Processes dialog messages and commands
- Registers/unregisters dialog windows with the 3DS Max core interface

## Key Types
- **FloaterDialogClass (Class)**: Main class for managing floating dialogs
- **HWND (Type)**: Windows handle for the dialog window
- **DLGPROC (Type)**: Dialog procedure callback type

## Key Functions
### _floater_dialog_proc
- Purpose: Global dialog procedure that routes messages to FloaterDialogClass instances
- Calls: `SetProp`, `GetProp`, `RemoveProp`, `FloaterDialogClass::Dialog_Proc`

### FloaterDialogClass::Create
- Purpose: Creates the floating dialog window and initializes child dialog parameters
- Calls: `Is_Created`, `CreateDialogParam`, `GetCOREInterface()->RegisterDlgWnd`

### FloaterDialogClass::Dialog_Proc
- Purpose: Handles dialog messages including child dialog creation and window sizing
- Calls: `CreateDialogParam`, `GetWindowRect`, `AdjustWindowRect`, `SetWindowPos`, `GetCOREInterface()->UnRegisterDlgWnd`

## Globals
- **AppInstance (HINSTANCE)**: Global application instance handle
- **IDD_W3DUTILITY_FLOATER_DIALOG (int)**: Resource ID for the floater dialog template

## Dependencies
- `floaterdialog.h` (header)
- `dllmain.h` (for AppInstance)
- `resource.h` (for dialog resource IDs)
- `<Max.h>` (3DS Max SDK)
- Windows API (dialog creation, message handling)
