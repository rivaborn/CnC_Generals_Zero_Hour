# Generals/Code/Tools/WW3D/max2w3d/boneicon.cpp - Enhanced Analysis

## Architectural Role
This file is part of the W3D model exporter toolchain, providing static mesh data for bone visualization in 3DS Max. It bridges the asset pipeline between Max plugins and the W3D runtime format.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/skin.cpp` (uses bone icon for skinning UI)
- `Generals/Code/Tools/WW3D/max2w3d/vxldbg.cpp` (debug visualization)
- `Generals/Code/Tools/WW3D/max2w3d/w3ddlg.cpp` (export dialog rendering)

### Outgoing
- None (pure data file, no external calls)

## Design Patterns
- **Data Module Pattern**: Encapsulates static mesh data for tooling
- **Literal Data Table**: Hardcoded vertex/face arrays for tool-specific visualization
- **Not inferable**: No runtime patterns evident (compile-time resource)

*Token count: 198*
