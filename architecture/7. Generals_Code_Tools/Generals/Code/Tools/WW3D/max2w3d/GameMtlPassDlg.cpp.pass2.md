# Generals/Code/Tools/WW3D/max2w3d/GameMtlPassDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for material pass editing in the Max2W3D exporter tool, bridging between 3ds Max's material editor and the W3D format's material system. It manages the tabbed dialog interface and delegates to specialized sub-dialogs for different material properties.

## Cross-References
### Incoming
- `GameMtlDlg` (parent dialog) - Creates and manages `GameMtlPassDlg` instances
- `GameMtl` - Provides material data and state management
- `IMtlParams` - Handles rollup page management and time tracking

### Outgoing
- `GameMtlShaderDlg`, `GameMtlTextureDlg`, `GameMtlVertexMaterialDlg`, `PS2GameMtlShaderDlg` - Sub-dialogs for specific material properties
- Windows API (`TabCtrl_*`, `SetWindowLong`, etc.) - For dialog creation and message handling
- `w3d_file.h` - Indirectly through material serialization

## Design Patterns
- **Composite Pattern**: The `GameMtlPassDlg` contains multiple sub-dialogs (`Page[]`) that are managed collectively
- **Bridge Pattern**: Separates the abstract material editing interface (`IMtlParams`) from its concrete implementation
- **Observer Pattern**: Dialog invalidation and reloading mechanism to keep UI in sync with material data

*Not inferable*: Exact implementation of material serialization to W3D format
