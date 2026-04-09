# Generals/Code/Tools/WW3D/max2w3d/genlodextensiondialog.cpp

## Purpose
Handles the LOD (Level of Detail) extension dialog for the Max2W3D tool, allowing users to configure LOD settings.

## Responsibilities
- Manages the dialog window for LOD extension options
- Handles user input for LOD index via spinner control
- Initializes and cleans up dialog resources
- Processes Windows messages for the dialog

## Key Types
- **GenLodExtensionDialogClass (Class)**: Manages the LOD extension dialog
- **OptionsStruct (Struct)**: Holds user-selected options (not defined here)
- **ISpinner (Type)**: 3DS Max spinner control interface

## Key Functions
### GenLodExtensionDialogClass::Get_Options
- Purpose: Displays the dialog and retrieves user input
- Calls: DialogBoxParam

### GenLodExtensionDialogClass::Dialog_Proc
- Purpose: Handles Windows messages for the dialog
- Calls: SetupIntSpinner, EndDialog

### _gen_lod_ext_dialog_proc
- Purpose: Windows dialog procedure that delegates to GenLodExtensionDialogClass
- Calls: GenLodExtensionDialogClass::Dialog_Proc

## Globals
- **AppInstance (HINSTANCE)**: Application instance handle (external)
- **IDD_GENERATE_LOD_EXTENSION_DIALOG (int)**: Dialog resource ID (external)
- **IDC_LOD_INDEX_SPIN (int)**: Spinner control ID (external)
- **IDC_LOD_INDEX_EDIT (int)**: Edit control ID (external)
- **MIN_LOD_INDEX (int)**: Minimum LOD index (external)
- **MAX_LOD_INDEX (int)**: Maximum LOD index (external)
- **INITIAL_LOD_INDEX (int)**: Default LOD index (external)

## Dependencies
- genlodextensiondialog.h
- dllmain.h
- resource.h
- <Max.h>
- External symbols: AppInstance, IDD_GENERATE_LOD_EXTENSION_DIALOG, IDC_LOD_INDEX_SPIN, IDC_LOD_INDEX_EDIT, MIN_LOD_INDEX, MAX_LOD_INDEX, INITIAL_LOD_INDEX
