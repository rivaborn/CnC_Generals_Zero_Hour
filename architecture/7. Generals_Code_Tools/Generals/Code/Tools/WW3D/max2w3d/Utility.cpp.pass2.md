# Generals/Code/Tools/WW3D/max2w3d/Utility.cpp - Enhanced Analysis

## Architectural Role
This file bridges MAXScript (3ds Max's scripting system) with the WW3D toolchain, exposing utility functions for path resolution and user interaction. It's part of the asset pipeline tools used to convert 3ds Max models into the W3D format.

## Cross-References
### Incoming
- MAXScript runtime calls `get_absolute_path_cf` and `input_box_cf` when executing corresponding script functions.
- `InputDlg` class (defined elsewhere) is instantiated here for dialog handling.

### Outgoing
- Calls into MAXScript API (`check_arg_count`, `type_check`, `key_arg`, `MAXScript_interface`).
- Uses `Create_Full_Path` (likely from a Windows API wrapper or custom utility).
- Depends on `util.h` and `InputDlg.h` for declarations.

## Design Patterns
- **Adapter Pattern**: Wraps MAXScript's limited API to provide familiar utility functions.
- **Command Pattern**: `input_box_cf` encapsulates a user interaction as a script-callable operation.
- **Not inferable**: No clear use of other patterns (e.g., no factories, observers, or decorators visible).

*Token count: 198*
