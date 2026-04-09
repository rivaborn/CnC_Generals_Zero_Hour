# Generals/Code/Tools/WW3D/max2w3d/hiersave.h - Enhanced Analysis

## Architectural Role
This file bridges 3DS Max's scene hierarchy with the W3D format, handling the serialization/deserialization of skeletal and object hierarchies. It's part of the asset pipeline tools that convert Max scenes into the engine's native format.

## Cross-References
### Incoming
- Likely called by Max plugin exporters (e.g., `max2w3d.cpp`) to export scene hierarchies
- Used by W3D model importers to reconstruct hierarchies

### Outgoing
- Depends on `ChunkSaveClass`/`ChunkLoadClass` for binary serialization
- Uses `INode` from Max SDK for scene graph traversal
- Relies on `W3dPivotStruct`/`W3dPivotFixupStruct` for transform data

## Design Patterns
- **Facade Pattern**: Abstracts Max's complex scene graph into a simpler hierarchy interface
- **Composite Pattern**: Manages hierarchical node relationships (parent/child)
- **Strategy Pattern**: Matrix fixup types (`MATRIX_FIXUP_*`) allow different transform correction strategies
