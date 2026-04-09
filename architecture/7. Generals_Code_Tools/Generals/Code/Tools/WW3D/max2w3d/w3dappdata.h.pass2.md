# Generals/Code/Tools/WW3D/max2w3d/w3dappdata.h - Enhanced Analysis

## Architectural Role
This header defines the metadata schema for W3D model export, acting as the bridge between 3DS Max's scene graph and the SAGE engine's asset pipeline. It encapsulates all exportable properties (geometry types, collision flags, etc.) and provides utility functions to query these properties during export.

## Cross-References
### Incoming
- `max2w3d` exporter tools (e.g., `w3dapp.cpp`) - uses utility functions to classify nodes
- MAXScript extensions (e.g., `WWScript.dlx`) - accesses app-data structures for model cloning
- W3D asset pipeline tools - reads app-data during model processing

### Outgoing
- **3DS Max SDK** (`<Max.h>`) - for `INode` access and app-data management
- **C runtime** (`strchr`) - for proxy detection via name parsing

## Design Patterns
- **Facade Pattern**: Utility functions (`Is_Bone`, `Is_Geometry`, etc.) abstract the bitfield manipulation in `W3DAppData2Struct`, hiding complexity from callers.
- **Flyweight Pattern**: App-data structures are stored per-node in 3DS Max's scene graph, reused across export operations.
- **Bitmask Enums**: Flags (`ExportFlagsEnum`, `GeometryFlagsEnum`) use bitwise operations for compact storage and efficient querying.
