# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_obsolete.h - Enhanced Analysis

## Architectural Role
This header serves as a legacy compatibility layer for the W3D rendering subsystem, documenting deprecated data structures and chunk IDs that were used in earlier versions of the engine. It acts as a reference for backward compatibility during model loading and asset conversion.

## Cross-References
### Incoming
- Likely referenced by `model.cpp` and other W3D loading code during legacy asset handling
- May be used by modding tools or asset converters that need to understand old formats

### Outgoing
- References basic W3D types (`W3dRGBStruct`, `W3dVectorStruct`) defined elsewhere in the subsystem
- No direct calls to other subsystems as it's purely declarative

## Design Patterns
- **Documentation Pattern**: The file serves as architectural documentation of deprecated features
- **Versioning Pattern**: Shows clear evolution of material formats (v1âv2âv3) through successive struct definitions
- **Chunk System**: Uses the engine's chunk-based serialization pattern for obsolete data formats

Not inferable: No runtime patterns visible as this is a header-only file with no implementation.
