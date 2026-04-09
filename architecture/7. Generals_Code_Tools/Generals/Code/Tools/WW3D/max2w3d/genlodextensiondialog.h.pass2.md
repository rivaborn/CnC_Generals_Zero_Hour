# Generals/Code/Tools/WW3D/max2w3d/genlodextensiondialog.h - Enhanced Analysis

## Architectural Role
This file defines a UI dialog for the Max2W3d tool, which is part of the asset pipeline for W3D model conversion. It bridges the 3DS Max plugin interface with the W3D exporter, allowing artists to configure LOD naming conventions.

## Cross-References
### Incoming
- Likely called by the Max2W3d exporter plugin when LOD configuration is needed
- May be referenced by other dialog classes in the Max2W3d toolset

### Outgoing
- Uses `Interface` class (3DS Max SDK interface)
- Uses `ISpinnerControl` (Max SDK control)
- Calls `_gen_lod_ext_dialog_proc` (internal callback)

## Design Patterns
- **Mediator Pattern**: The dialog class mediates between the Max interface and the spinner control
- **Data Transfer Object**: `OptionsStruct` serves as a DTO for configuration data
- **Not inferable**: No clear observer or factory patterns visible in header

*Token count: 198*
