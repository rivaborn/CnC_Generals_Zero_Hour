# Generals/Code/Tools/WW3D/max2w3d/genmtlnamesdialog.cpp - Enhanced Analysis

## Architectural Role
This file is part of the Max2W3D toolchain, bridging 3DS Max and the W3D asset pipeline. It handles user input for material naming conventions, critical for consistent asset organization in the SAGE engine's W3D format.

## Cross-References
### Incoming
- Called by Max2W3D's asset export pipeline when material names need user configuration
- Likely invoked from the main Max2W3D plugin entry point (not shown in file)

### Outgoing
- Calls 3DS Max SDK functions (Interface, ISpinner) for UI integration
- Uses Windows API for dialog management
- References W3D-specific constants (W3D_NAME_LEN) from w3d_file.h

## Design Patterns
- **Bridge Pattern**: Decouples dialog UI from business logic via the static _gen_mtl_names_dialog_proc delegate
- **Command Pattern**: Dialog actions (OK/Cancel) encapsulate user input as OptionsStruct
- **Template Method**: Dialog_Proc handles WM_INITDIALOG/WM_COMMAND in a fixed sequence

*Not inferable*: No clear use of Observer or Factory patterns despite UI-heavy nature.
