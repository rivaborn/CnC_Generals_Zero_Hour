# Generals/Code/Tools/WW3D/max2w3d/ExportAllDlg.cpp - Enhanced Analysis

## Architectural Role
This file is part of the asset pipeline tooling for the SAGE engine, specifically handling the UI for exporting 3D assets from 3DS Max to the W3D format. It bridges the 3DS Max SDK with the engine's asset conversion workflow.

## Cross-References
### Incoming
- Likely called from the main max2w3d tool's UI flow (not explicitly shown in this file)
- 3DS Max SDK (`Interface` class) provides the parent window handle

### Outgoing
- Calls into Windows API (`DialogBoxParam`, `SHBrowseForFolder`)
- Uses 3DS Max SDK (`Interface::GetMAXHWnd()`)
- No direct calls to W3D-specific code (export logic is likely in other files)

## Design Patterns
- **Dialog Controller**: The `ExportAllDlg` class encapsulates both the dialog state and its behavior
- **Thunk Pattern**: Uses `_thunk_dialog_proc` to adapt between Windows' `DLGPROC` and the class's `DialogProc` method
- **MVC Lite**: Separates dialog presentation (`DialogProc`) from business logic (`OnOK`, `OnBrowse`)

*Not inferable*: No clear use of Factory, Observer, or other patterns in this snippet.
