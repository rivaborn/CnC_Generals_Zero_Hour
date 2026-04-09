# Generals/Code/Tools/WW3D/max2w3d/genlodextensiondialog.h

## Purpose
Defines a dialog class for configuring LOD (Level of Detail) extension naming parameters in the Max2W3d tool.

## Responsibilities
- Manages a dialog for LOD extension naming options
- Handles user input for LOD index via spinner control
- Provides access to selected options via `Get_Options`
- Implements dialog procedure for Windows message handling

## Key Types
- **GenLodExtensionDialogClass (Class)**: Main dialog class for LOD extension parameters
- **OptionsStruct (Struct)**: Holds user-selected LOD options (LOD index)
- **(anonymous enum) (Enum)**: Defines LOD index bounds (MIN/MAX/INITIAL)
- **Interface (Class)**: Reference to Max interface (external)
- **ISpinnerControl (Class)**: Reference to spinner control (external)

## Key Functions
### GenLodExtensionDialogClass()
- Purpose: Constructor initializes dialog with Max interface
- Calls: None

### Get_Options()
- Purpose: Retrieves user-selected options from dialog
- Calls: None

### Dialog_Proc()
- Purpose: Handles Windows messages for the dialog
- Calls: None

## Globals
- **Hwnd (HWND)**: Stores dialog window handle
- **Options (OptionsStruct*)**: Pointer to options structure
- **MaxInterface (Interface*)**: Reference to Max interface
- **LodIndexSpin (ISpinnerControl*)**: Reference to spinner control

## Dependencies
- `<windows.h>` for Windows API types
- `Interface` class (external)
- `ISpinnerControl` class (external)
- `_gen_lod_ext_dialog_proc` callback (external)
