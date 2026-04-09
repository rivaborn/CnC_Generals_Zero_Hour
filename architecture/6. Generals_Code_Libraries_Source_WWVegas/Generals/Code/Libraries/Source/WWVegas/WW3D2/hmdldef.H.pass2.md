# Generals/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.H - Enhanced Analysis

## Architectural Role
This file defines the core data structures and class for hierarchy model definitions in the SAGE engine's W3D rendering subsystem. It serves as the blueprint for creating runtime hierarchy models, bridging the asset pipeline with the rendering system.

## Cross-References
### Incoming
- `HModelClass` and `HLodClass` (friends) access private members
- Asset management system uses this for model instantiation
- Rendering pipeline references `HmdlNodeDefStruct` for object attachment

### Outgoing
- Uses `ChunkLoadClass` for W3D file parsing
- References `SnapPointsClass` for attachment points
- Depends on `w3d_file.h` for W3D format constants

## Design Patterns
- **Factory Pattern**: `HModelDefClass` acts as a blueprint for creating runtime `HModelClass` instances
- **Composite Pattern**: Hierarchy model structure with sub-objects and connections
- **Resource Management**: Explicit `Free()` method for cleanup (manual memory management pattern)
