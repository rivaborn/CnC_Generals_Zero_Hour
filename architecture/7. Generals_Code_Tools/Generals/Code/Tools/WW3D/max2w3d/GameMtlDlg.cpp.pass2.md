# Generals/Code/Tools/WW3D/max2w3d/GameMtlDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for the W3D material editor plugin in 3DS Max, bridging MAX's material system with the game's W3D format. It manages the dialog infrastructure for material properties while delegating material logic to GameMtl.

## Cross-References
### Incoming
- `GameMtl` calls `SetParamDlg` to register this dialog
- `GameMtlPassDlg` instances call back to parent dialog for updates
- MAX SDK calls dialog procedures (`DisplacementMapDlgProc`, `SurfaceTypePanelDlgProc`, etc.)

### Outgoing
- Calls into `GameMtl` for material property access/modification
- Uses MAX SDK (`IParams`) for dialog management
- Creates `GameMtlPassDlg` instances for per-pass editing

## Design Patterns
- **Bridge Pattern**: Separates material abstraction (`GameMtl`) from UI implementation
- **Observer Pattern**: Dialog updates material state when UI changes occur
- **Composite Pattern**: Manages collection of pass dialogs (`PassDialog[]`) as part of material editing

*Not inferable*: Exact relationship with W3D export pipeline not visible in this file.
