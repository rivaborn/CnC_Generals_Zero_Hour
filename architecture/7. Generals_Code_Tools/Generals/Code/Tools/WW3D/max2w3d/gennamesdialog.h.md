# Generals/Code/Tools/WW3D/max2w3d/gennamesdialog.h

## Purpose
Defines a dialog class for configuring node naming parameters in the Max2W3D tool.

## Responsibilities
- Manages a dialog for setting naming options (root name, prefix, suffix, collision bits)
- Handles user input for name generation parameters
- Provides access to naming configuration via `OptionsStruct`
- Controls dialog behavior (validation, toggles)

## Key Types
- **GenNamesDialogClass (Class)**: Main dialog class for node naming parameters.
- **OptionsStruct (Struct)**: Holds naming configuration options (root/prefix/suffix names, collision bits, selection scope).
- **(anonymous enum) (Enum)**: Defines constant values for name index ranges and string length limits.

## Key Functions
### GenNamesDialogClass()
- Purpose: Constructor for the dialog class.
- Calls: None visible.

### Get_Options()
- Purpose: Retrieves the current naming options from the dialog.
- Calls: None visible.

### Dialog_Proc()
- Purpose: Handles Windows messages for the dialog.
- Calls: None visible.

### Ok_To_Exit()
- Purpose: Validates if the dialog can be closed.
- Calls: None visible.

### Toggle_Collision_Bits_Assignment()
- Purpose: Toggles collision bit assignment settings.
- Calls: None visible.

### Toggle_Name_Assignment()
- Purpose: Toggles name assignment settings.
- Calls: None visible.

## Globals
- **Hwnd (HWND)**: Stores the dialog window handle.
- **Options (OptionsStruct*)**: Pointer to the current naming options.
- **MaxInterface (Interface*)**: Reference to the 3DS Max interface.
- **NameIndexSpin (ISpinnerControl*)**: Spinner control for the name index.

## Dependencies
- `<Max.h>`:
