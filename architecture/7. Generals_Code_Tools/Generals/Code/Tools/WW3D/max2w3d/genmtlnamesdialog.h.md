# Generals/Code/Tools/WW3D/max2w3d/genmtlnamesdialog.h

## Purpose
Defines a dialog class for configuring material naming parameters in the Max2W3d tool.

## Responsibilities
- Manages a dialog for material naming options
- Handles user input for naming parameters
- Provides access to naming configuration options
- Validates dialog exit conditions

## Key Types
- **GenMtlNamesDialogClass (Class)**: Main dialog class for material naming parameters
- **OptionsStruct (Struct)**: Contains material naming options (root name, index, selection flag)
- **(anonymous enum) (Enum)**: Defines constant values for naming parameters

## Key Functions
### GenMtlNamesDialogClass()
- Purpose: Constructor for the dialog class
- Calls: None

### Get_Options()
- Purpose: Retrieves the current naming options from the dialog
- Calls: None

### Dialog_Proc()
- Purpose: Handles Windows messages for the dialog
- Calls: None

### Ok_To_Exit()
- Purpose: Validates if the dialog can be closed
- Calls: None

## Globals
- None

## Dependencies
- `<windows.h>` for Windows API types
- `Interface` class (forward declared)
- `ISpinnerControl` class (forward declared)
