# Generals/Code/Tools/WW3D/max2w3d/SceneSetupDlg.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for the max2w3d tool's scene configuration dialog, bridging the 3DS Max plugin interface with the W3D export pipeline. It encapsulates dialog management and data validation for LOD/damage settings.

## Cross-References
### Incoming
- Likely called by max2w3d's main plugin code (e.g., `max2w3d.cpp`) to show the scene setup dialog during export workflow.

### Outgoing
- References `Interface` class (3DS Max SDK wrapper) for plugin communication
- Uses Win32 API (`HWND`, `DialogProc`) for dialog management
- Relies on `Resource.h` for dialog template definitions

## Design Patterns
- **Dialog Controller**: Encapsulates UI state and message handling
- **Data Accessor Methods**: `GetEditXxx`/`SetEditXxx` pattern for controlled dialog control access
- **Resource-Based UI**: Uses Win32 dialog resources (IDD) for UI definition

*Not inferable*: No clear use of observer pattern or strategy pattern for damage/LOD processing.
