# Generals/Code/Tools/WW3D/max2w3d/w3ddlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for the W3D export tool, bridging between the 3DS Max plugin interface and the export pipeline. It handles user configuration of export parameters while maintaining compatibility with the SAGE engine's asset pipeline requirements.

## Cross-References
### Incoming
- Called by the Max2W3D plugin's export workflow when user initiates W3D export
- Used by the preset export dialog system (PresetExportOptionsDialogClass)

### Outgoing
- Calls into `w3dexp.h` for export execution
- Uses `rawfile.h` for file I/O operations
- Interfaces with Max SDK through `Interface` and `ExpInterface` parameters

## Design Patterns
- **Bridge Pattern**: Separates abstraction (export options) from implementation (dialog UI)
- **Observer Pattern**: UI elements react to state changes (e.g., radio button selections enabling/disabling controls)
- **Facade Pattern**: Simplifies complex export configuration through a dialog interface

*Not inferable*: Exact relationship with animation compression pipeline (ANIM_FLAVOR_* constants)
