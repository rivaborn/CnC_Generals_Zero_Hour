# Generals/Code/Tools/WW3D/max2w3d/meshsave.h - Enhanced Analysis

## Architectural Role
This header defines the core mesh export functionality for the W3D exporter tool, bridging 3ds Max's mesh data structures with the W3D format used by the game engine. It handles the conversion of geometric data, materials, and shaders while maintaining compatibility with the game's rendering pipeline.

## Cross-References
### Incoming
- `max2w3d.cpp` (main exporter tool) - likely instantiates `MeshSaveClass` and calls `Write_To_File()`
- `meshbuild.h` - `MeshBuilderClass` is used internally by `Build_Mesh()`
- `w3dmtl.h` - material handling dependencies

### Outgoing
- **W3D File Format Subsystem**: Writes to `ChunkSaveClass` via multiple `write_*()` methods
- **Material System**: Calls into `W3dMaterialDescClass` for material processing
- **Hierarchy System**: Uses `HierarchySaveClass` for bone/skeleton data
- **Skinning System**: Interfaces with `SkinDataClass` for deformation data

## Design Patterns
- **Facade Pattern**: `MeshSaveClass` provides a simplified interface to the complex mesh export process
- **Builder Pattern**: Uses `MeshBuilderClass` to construct mesh data incrementally
- **Strategy Pattern**: Different `write_*()` methods implement specific export strategies for various mesh components

*Not inferable*: Exact implementation details of patterns without seeing the .cpp file.
