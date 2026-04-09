# Generals/Code/Tools/WW3D/max2w3d/gennamesdialog.cpp

## Purpose
Handles the "Generate Names" dialog in the Max2W3D tool, allowing users to configure naming and collision settings for 3D models.

## Responsibilities
- Manages dialog creation and user input validation
- Controls enabling/disabling of dialog controls based on user selections
- Populates an OptionsStruct with user preferences
- Handles spin controls for numeric input

## Key Types
- **GenNamesDialogClass (Class)**: Main dialog handler class
- **OptionsStruct (Struct)**: Stores user configuration options
- **Interface (Type)**: Reference to 3DS Max interface (external)

## Key Functions
### GenNamesDialogClass::Get_Options
- Purpose: Displays dialog and retrieves user options
- Calls: DialogBoxParam, _gen_names_dialog_proc

### GenNamesDialogClass::Dialog_Proc
- Purpose: Windows dialog procedure handler
- Calls: SetupIntSpinner, SendDlgItemMessage, CheckDlgButton, GetWindowText, EndDialog, Toggle_Name_Assignment, Toggle_Collision_Bits_Assignment

### _gen_names_dialog_proc
- Purpose: Static thunk function that routes messages to class instance
- Calls: GenNamesDialogClass::Dialog_Proc

## Globals
- **AppInstance (HINSTANCE)**: Application instance handle (external)
- **IDD_GENERATE_NAMES_DIALOG (INT)**: Dialog resource ID (external)

## Dependencies
- gennamesdialog.h (header)
- dllmain.h (external)
- resource.h (external)
- Windows API (HWND, WPARAM, LPARAM, etc.)
- 3DS Max SDK types (Interface)
