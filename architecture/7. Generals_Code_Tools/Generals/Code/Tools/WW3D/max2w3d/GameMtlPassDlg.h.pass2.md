# Generals/Code/Tools/WW3D/max2w3d/GameMtlPassDlg.h - Enhanced Analysis

## Architectural Role
This file defines the UI dialog for editing material passes in the Max2W3d asset conversion tool, bridging between 3DS Max's material editor and the W3D format's material system. It's part of the asset pipeline tooling that supports the game's rendering pipeline.

## Cross-References
### Incoming
- Likely called by the Max2W3d tool's main dialog system when material editing is initiated
- Probably referenced by the material editor's tab control system

### Outgoing
- Calls into `GameMtl` for material data access
- Uses `GameMtlFormClass` for page-specific UI handling
- Interfaces with 3DS Max's `IMtlParams` for material editor integration

## Design Patterns
- **Bridge Pattern**: Separates material data (`GameMtl`) from its UI representation (this dialog)
- **Composite Pattern**: Manages multiple editing pages (`GameMtlFormClass` instances) as a unified interface
- **Observer Pattern**: Notifies material editor of changes via `IParams->MtlChanged()`
