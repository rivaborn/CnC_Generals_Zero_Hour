# Generals/Code/Tools/WW3D/max2w3d/ExportAllDlg.h - Enhanced Analysis

## Architectural Role
This file defines the UI layer for the max2w3d asset export tool, bridging between the 3DS Max SDK (via `Interface`) and the export pipeline. It handles user input for directory selection and export options, serving as the primary interaction point for artists during the W3D conversion process.

## Cross-References
### Incoming
- Likely called by the main max2w3d plugin entry point (not shown in file)
- Potentially referenced by other dialog classes in the tool suite

### Outgoing
- Interfaces with 3DS Max via `Interface` class
- Uses Windows API for dialog management
- References resource definitions from `resource.h`

## Design Patterns
- **MVC (Model-View-Controller)**: Separates dialog UI (view) from export logic (controller), with `Interface` acting as the model
- **Dialog Proc Pattern**: Uses Windows' message loop pattern for UI event handling
- **Resource-Based UI**: Leverages external resource definitions for localization and maintainability

*Not inferable*: No clear use of factory, observer, or strategy patterns in this header.
