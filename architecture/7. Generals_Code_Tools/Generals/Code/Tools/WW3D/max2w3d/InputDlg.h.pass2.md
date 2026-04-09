# Generals/Code/Tools/WW3D/max2w3d/InputDlg.h - Enhanced Analysis

## Architectural Role
This file defines a lightweight dialog wrapper used by the max2w3d toolchain for MAXScript integration. It bridges the 3DS Max plugin interface with the W3D export pipeline, handling user input during asset conversion.

## Cross-References
### Incoming
- `max2w3d.cpp` (likely calls `DoModal()` for user prompts during export)
- MAXScript host (via `_thunk_dialog_proc` for script callbacks)

### Outgoing
- Windows API (dialog creation, message handling)
- Resource system (via `resource.h` for dialog templates)

## Design Patterns
- **Adapter Pattern**: Wraps Windows dialog procedures to provide a C++ interface for MAXScript
- **MVC Lite**: Separates dialog data (`m_Value`, `m_Label`) from presentation logic (`DialogProc`)
- **Resource-Based UI**: Uses pre-defined dialog templates from `resource.h` (not inferable which specific resources)
