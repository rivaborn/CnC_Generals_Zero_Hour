# Generals/Code/Tools/WW3D/max2w3d/FormClass.h - Enhanced Analysis

## Architectural Role
This file defines a base class for dialog forms in the max2w3d tool, which is part of the asset pipeline for converting 3DS Max models into the W3D format used by the SAGE engine. It bridges the 3DS Max SDK with custom tooling for model export.

## Cross-References
### Incoming
- Likely called by max2w3d tool's UI classes (e.g., export dialogs, property editors)
- May be referenced by other tool-specific dialog implementations

### Outgoing
- Inherits from `ParamDlg` (3DS Max SDK)
- Uses Windows API for dialog creation and management
- Relies on `Max.h` for 3DS Max integration

## Design Patterns
- **Template Method**: `Dialog_Proc` is a pure virtual function, enforcing a contract for derived classes to implement message handling.
- **Adapter**: Acts as an adapter between 3DS Max's `ParamDlg` and custom tool dialogs.
- **Not inferable**: No clear use of other patterns without seeing derived classes.
