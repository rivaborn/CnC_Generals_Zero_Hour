# Generals/Code/Tools/WW3D/max2w3d/InputDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements a lightweight modal dialog wrapper for the max2w3d tool, serving as a utility for collecting user input during 3D model conversion. It bridges the Windows API with the tool's internal workflow, handling text input validation and dialog management.

## Cross-References
### Incoming
- Likely called by max2w3d's main tool logic when user input is required (e.g., for file paths or parameter values)
- Potentially referenced by other tool dialogs needing similar input patterns

### Outgoing
- Uses Windows API (DialogBoxParam, SetWindowText, etc.)
- Relies on dialog resources defined in .rc files (IDD, IDC_LABEL, IDC_VALUE)
- Depends on AppInstance global for dialog creation

## Design Patterns
- **Adapter Pattern**: Wraps Windows dialog procedures into a C++ class interface, abstracting platform-specific details
- **Command Pattern**: Encapsulates dialog actions (OK/Cancel) as methods (OnOK, OnInitDialog) for deferred execution
- **Thunking**: Uses `_thunk_dialog_proc` to bridge C++ class methods with Windows callback conventions

*Not inferable*: No observable use of Observer, Factory, or other patterns.
