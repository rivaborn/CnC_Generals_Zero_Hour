# Generals/Code/Tools/WW3D/max2w3d/FormClass.cpp

## Purpose
Handles creation and management of dialog forms in the max2w3d tool, including resource loading and initialization.

## Responsibilities
- Creates dialog windows from resource templates
- Manages dialog procedures and message handling
- Initializes dialog controls with resource data
- Handles Windows-specific dialog initialization

## Key Types
- **FormClass (Class)**: Base class for dialog forms, managing window creation and message processing

## Key Functions
### Create_Form
- Purpose: Creates a dialog window from a resource template
- Calls: `CreateDialogParam`, `SetWindowLong`, `GetWindowRect`, `ExecuteDlgInit`

### fnFormProc
- Purpose: Windows procedure that routes messages to the virtual Dialog_Proc
- Calls: `GetProp`, `SetProp`, `RemoveProp`, `Dialog_Proc`

### ExecuteDlgInit (resource name version)
- Purpose: Loads and executes dialog initialization resource
- Calls: `FindResource`, `LoadResource`, `LockResource`, `ExecuteDlgInit` (LPVOID version), `UnlockResource`, `FreeResource`

### ExecuteDlgInit (LPVOID version)
- Purpose: Processes dialog initialization data to populate controls
- Calls: `SendDlgItemMessageA`

## Globals
- **AppInstance (HINSTANCE)**: Global application instance handle

## Dependencies
- `FormClass.H`
- `Dllmain.H`
- Windows API: `CreateDialogParam`, `SetWindowLong`, `GetWindowRect`, `FindResource`, `LoadResource`, `LockResource`, `UnlockResource`, `FreeResource`, `SendDlgItemMessageA`, `GetProp`, `SetProp`, `RemoveProp`
- MFC-style dialog initialization resource handling
