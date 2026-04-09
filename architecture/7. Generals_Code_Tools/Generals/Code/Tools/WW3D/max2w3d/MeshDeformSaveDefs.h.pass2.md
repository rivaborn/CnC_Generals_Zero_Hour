# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSaveDefs.h - Enhanced Analysis

## Architectural Role
This header defines the binary serialization format for mesh deformation data in the 3DS Max export pipeline. It serves as the contract between the Max plugin (max2w3d) and the W3D runtime, ensuring consistent deformation data representation across tools and engine.

## Cross-References
### Incoming
- `MeshDeformData.cpp` (uses these structs for serialization)
- Other max2w3d export tools (references chunk IDs for validation)

### Outgoing
- None (pure declarations)

## Design Patterns
- **Chunked Binary Format**: Uses a chunk-based structure (similar to RIFF/WAV) for extensibility in deformation data storage
- **Fixed-Layout Structs**: Uses POD structs with explicit padding (reserved fields) for binary compatibility across platforms
- **Enum-Based Versioning**: Chunk IDs act as implicit version markers for format evolution

Key insight: The `DEFORM_SET_MANUAL_DEFORM` flag suggests runtime support for both automatic (physics-based) and manual vertex deformations, indicating the engine likely has dual deformation pipelines.
