# Generals/Code/Tools/WW3D/max2w3d/w3dutil.h - Enhanced Analysis

## Architectural Role
This header bridges the 3ds Max plugin infrastructure and the W3D export pipeline, defining the contract for export options and node metadata access. It serves as the central registry for W3D-specific AppData structures, enabling MAXScript automation and batch processing.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/w3dutil.cpp` (implementation)
- `Generals/Code/Tools/WW3D/max2w3d/w3dexport.cpp` (export logic)
- `Generals/Code/Tools/WW3D/max2w3d/wwscript.dlx` (MAXScript integration)

### Outgoing
- `utilapi.h` (MAX SDK utilities)
- `w3dappdata.h` (AppData structure definitions)
- `dllmain.h` (plugin registration)

## Design Patterns
- **Registry Pattern**: Centralized accessors for AppData structures enable dynamic discovery by MAXScript.
- **Data Transfer Object**: `W3dExportOptionsStruct` encapsulates export configuration for serialization/deserialization.
- **Facade**: Hides complexity of 3ds Max node metadata behind simple accessor functions.
