# Generals/Code/Tools/WW3D/max2w3d/SceneSetupDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for the max2w3d asset pipeline tool, specifically handling scene export configuration. It bridges the 3DS Max SDK with the W3D export pipeline, allowing artists to configure LOD and damage model generation parameters.

## Cross-References
### Incoming
- Called by max2w3d tool's export workflow (not shown in file)
- Likely invoked from the main max2w3d plugin interface

### Outgoing
- Uses 3DS Max SDK (`Interface` class) for dialog hosting
- Calls Windows API for dialog management
- Interfaces with other max2w3d components via the `Interface` parameter

## Design Patterns
- **Dialog Controller**: Encapsulates dialog state and behavior
- **Thunk Pattern**: Uses `_thunk_dialog_proc` to adapt between Windows callback and member function
- **Data Transfer Object**: Maintains export configuration state (LOD/Damage counts/offsets/procedures)
