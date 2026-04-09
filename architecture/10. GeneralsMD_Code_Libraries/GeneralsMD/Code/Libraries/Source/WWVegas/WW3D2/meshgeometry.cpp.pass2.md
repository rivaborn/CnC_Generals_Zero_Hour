# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.cpp - Enhanced Analysis

## Architectural Role
Core 3D mesh management component in the SAGE engine's rendering pipeline. Handles mesh loading, spatial queries, and skinning operations that feed into both rendering and physics systems.

## Cross-References
### Incoming
- Rendering system (uses `get_deformed_screenspace_vertices` for vertex transformation)
- Physics system (uses collision detection methods like `Cast_Ray`)
- Animation system (uses `get_deformed_vertices` for skinning)

### Outgoing
- **AABTreeClass**: For spatial partitioning (culling tree generation)
- **HTreeClass**: For hierarchical bone transformations in skinning
- **VectorProcessorClass**: For SIMD-optimized vertex transformations
- **W3D file I/O**: For asset loading

## Design Patterns
- **Resource Pooling**: Uses global `_PlaneEQArray` and `_VNormArray` for temporary storage to reduce allocations
- **Strategy Pattern**: Different collision detection methods (`cast_ray_brute_force`, `cast_aabox_z90`) can be selected based on context
- **Flyweight Pattern**: Mesh data (vertices, normals) is stored once and referenced by multiple instances

**Note**: The `Scale` method demonstrates optimization by preserving the culling tree when scaling uniformly, avoiding expensive regeneration.
