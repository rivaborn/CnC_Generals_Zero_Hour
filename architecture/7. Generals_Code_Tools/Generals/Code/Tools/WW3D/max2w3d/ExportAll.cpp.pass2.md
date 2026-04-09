# Generals/Code/Tools/WW3D/max2w3d/ExportAll.cpp - Enhanced Analysis

## Architectural Role
This file bridges the MAXScript scripting environment with the W3D export pipeline, enabling artists to configure export settings via a dialog. It acts as a thin adapter layer between 3ds Max's MAXScript API and the export tool's internal logic.

## Cross-References
### Incoming
- Called by MAXScript when `wwExportTreeSettings` is invoked (e.g., from artist scripts or export workflows).

### Outgoing
- Calls into `ExportAllDlg` for UI interaction.
- Uses MAXScript API functions (`check_arg_count`, `type_check`, etc.) for argument validation and value conversion.

## Design Patterns
- **Adapter Pattern**: Converts MAXScript array arguments to C++ types and vice versa, mediating between scripting and native code.
- **Command Pattern**: Encapsulates the export settings dialog as a reusable operation (`ExportAllDlg`).
- **Factory Pattern**: Dynamically creates MAXScript `Array` and `String` objects for return values.

*Not inferable*: No explicit use of Observer or Strategy patterns.
