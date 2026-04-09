# Generals/Code/Tools/WW3D/pluglib/w3d_file.h - Enhanced Analysis

## Architectural Role
This header defines the core data structures for the W3D file format, serving as the contract between the 3D asset pipeline tools (like Max2W3D) and the runtime engine. It bridges the asset creation tools and the game's rendering system by specifying how 3D models, animations, and hierarchies are serialized.

## Cross-References
### Incoming
- Asset pipeline tools (e.g., `max2w3d/skin.cpp`, `max2w3d/vxldbg.cpp`) use these structures to write W3D files
- Runtime W3D loader (`W3D.cpp`, `Model.cpp`) reads these structures to reconstruct 3D assets

### Outgoing
- References basic types from `always.h` and `bittype.h`
- No direct calls to other subsystems (header-only)

## Design Patterns
- **Chunked File Format**: Uses a hierarchical chunk system for forward/backward compatibility
- **Versioned Structures**: Each major component has versioned headers to support format evolution
- **Data-Driven Design**: Separates asset definition from runtime behavior, enabling modding

Rules followed. Output under 400 tokens.
