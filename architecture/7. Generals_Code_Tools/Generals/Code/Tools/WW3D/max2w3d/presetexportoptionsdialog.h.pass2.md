# Generals/Code/Tools/WW3D/max2w3d/presetexportoptionsdialog.h - Enhanced Analysis

## Architectural Role
This file defines the UI layer for the Max2W3d export tool, bridging 3DS Max's plugin architecture with W3D asset pipeline configuration. It encapsulates export preset management, exposing a modal dialog for artists to configure W3D-specific settings before asset conversion.

## Cross-References
### Incoming
- **max2w3d plugin**: Likely instantiates this dialog when exporting assets
- **W3D export pipeline**: Uses the configured options (W3dExportOptionsStruct) during conversion

### Outgoing
- **Windows API**: Direct HWND-based dialog management
- **3DS Max SDK**: Uses Interface* for Max integration
- **w3dutil.h**: For W3dExportOptionsStruct definition

## Design Patterns
- **MVC (Model-View-Controller)**: Separates export options (model) from UI controls (view) and message handlers (controller)
- **Strategy Pattern**: Different pane types (PANE_HLOD, PANE_ANIM) represent interchangeable export strategies
- **Command Pattern**: On_Command() handles UI events as discrete commands

*Not inferable*: Exact relationship with W3D asset pipeline or how options are applied post-export.
