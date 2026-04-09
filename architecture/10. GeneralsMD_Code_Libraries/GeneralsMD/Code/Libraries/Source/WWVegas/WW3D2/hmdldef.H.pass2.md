# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.H - Enhanced Analysis

## Architectural Role
This file defines the core data structures and class for hierarchy model definitions in the SAGE engine's W3D rendering subsystem. It serves as the blueprint for creating hierarchical models, bridging the static model definition (HModelDefClass) with runtime instances (HModelClass).

## Cross-References
### Incoming
- `HModelClass` (friend declaration) - Uses private members of HModelDefClass
- `HLodClass` (friend declaration) - Also accesses private members
- Asset management system - Likely instantiates HModelDefClass objects

### Outgoing
- `ChunkLoadClass` - Used for loading W3D file chunks
- `SnapPointsClass` - Manages attachment points for sub-objects
- `w3d_file.h` - For W3D file format definitions

## Design Patterns
- **Factory Pattern**: HModelDefClass acts as a blueprint for creating HModelClass instances
- **Composite Pattern**: Manages hierarchical relationships between model components
- **Resource Management**: Uses explicit Free() method for cleanup (manual memory management pattern)
