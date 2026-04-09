# Generals/Code/Tools/ImagePacker/Include/ImageInfo.h - Enhanced Analysis

## Architectural Role
This header defines the core data structure for the ImagePacker tool, bridging the asset pipeline with the SAGE engine's texture system. It encapsulates metadata for individual images during the texture atlas generation process, serving as the primary interface between the packing algorithm and the final W3D texture format.

## Cross-References
### Incoming
- **ImagePacker tool**: Uses `ImageInfo` to track image state during packing
- **TexturePage management**: Likely instantiated by texture atlas generation code
- **Asset build pipeline**: Consumes this struct to populate packed texture data

### Outgoing
- **TexturePage class**: References via pointer for page assignment
- **BaseType.h**: Uses fundamental types (Int, UnsignedInt, etc.)
- **Packing algorithm**: Provides fitting parameters via `m_fitBits` and `m_gutterUsed`

## Design Patterns
- **Data Transfer Object (DTO)**: Pure data container for image metadata
- **Linked List**: Uses `m_nextPageImage`/`m_prevPageImage` for per-page image ordering
- **Bitmask Flags**: Status and fitting parameters encoded as enums for compact storage
