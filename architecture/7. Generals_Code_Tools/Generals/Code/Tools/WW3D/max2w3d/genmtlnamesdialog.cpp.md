# Generals/Code/Tools/WW3D/max2w3d/genmtlnamesdialog.cpp

## Purpose
Handles a dialog for generating material names in the Max2W3D tool, allowing users to configure naming options.

## Responsibilities
- Manages the material naming dialog UI
- Validates user input
- Configures naming options (root name, index, scope)
- Integrates with 3DS Max via its SDK

## Key Types
- **GenMtlNamesDialogClass** (Class): Manages the dialog and user input
- **OptionsStruct** (Struct): Holds user-selected naming options
- **ISpinner** (Type): 3DS Max spinner control for numeric input

## Key Functions
### GenMtlNamesDialogClass::Get_Options
- Purpose: Displays the dialog and retrieves user options
- Calls: DialogBoxParam

### GenMtlNamesDialogClass::Ok_To_Exit
- Purpose: Validates user input before accepting
- Calls: GetWindowText, MessageBox

### GenMtlNamesDialogClass::Dialog_Proc
- Purpose: Handles Windows messages for the dialog
- Calls: SetupIntSpinner, GetWindowText, CheckDlgButton, EndDialog

### _gen_mtl_names_dialog_proc
- Purpose: Windows dialog procedure that delegates to GenMtlNamesDialogClass
- Calls: GenMtlNamesDialogClass::Dialog_Proc

## Globals
- **AppInstance** (HINSTANCE): Application instance handle
- **IDD_GENERATE_MTL_NAMES_DIALOG** (Resource ID): Dialog resource identifier

## Dependencies
- genmtlnamesdialog.h
- dllmain.h
- resource.h
- w3d_file.h
- <Max.h> (3DS Max SDK)
- Windows API (HWND, WPARAM, LPARAM, etc.)
