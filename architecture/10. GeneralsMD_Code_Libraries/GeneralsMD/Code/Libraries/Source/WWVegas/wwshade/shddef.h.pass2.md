# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddef.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for shader definitions in the SAGE engine's rendering pipeline, serving as the bridge between shader metadata and hardware-specific implementations. It encapsulates shader versioning, capabilities, and the factory pattern for shader instantiation, critical for the engine's cross-platform rendering support.

## Cross-References
### Incoming
- Rendering subsystem (e.g., `wwshade` implementations)
- Asset loading pipeline (uses `ChunkSaveClass`/`ChunkLoadClass`)
- Editor tools (via `EditableClass` inheritance)

### Outgoing
- `ShdInterfaceClass` (hardware-specific shader implementations)
- `shdclassids.h` (for class ID definitions)
- `StringClass` (for name storage)

## Design Patterns
- **Abstract Factory**: `Create()` method decouples shader definition from implementation.
- **Composite**: `ShdDefClass` aggregates shader parameters (textures, colors) as editable properties.
- **Strategy**: Capability queries (`Uses_Vertex_Alpha`, etc.) allow runtime shader selection.

*Not inferable*: Exact relationship with `ShdInterfaceClass` or version-specific implementations.
