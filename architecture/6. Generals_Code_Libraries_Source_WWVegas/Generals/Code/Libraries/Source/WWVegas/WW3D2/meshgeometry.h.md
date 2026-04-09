# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.h

## Purpose
Defines the `MeshGeometryClass` for handling 3D mesh geometry data, including vertices, polygons, normals, and collision detection.

## Responsibilities
- Manages mesh geometry data (vertices, polygons, normals, etc.)
- Provides collision detection and intersection tests
- Handles W3D file format loading for mesh data
- Supports bounding volumes and culling trees
- Maintains flags for mesh properties (e.g., two-sided, cast shadow)

## Key Types
- **MeshGeometryClass (Class)**: Core class for mesh geometry data and operations.
- **FlagsType (Enum)**: Bit flags for mesh properties (e.g., `DIRTY_BOUNDS`, `TWO_SIDED`).

## Key Functions
### `Reset_Geometry`
- Purpose: Resets mesh geometry with given polygon and vertex counts.
- Calls: None (initializes internal buffers).

### `Load_W3D`
- Purpose: Loads mesh data from a W3D file chunk.
- Calls: `read_chunks`, `read_vertices`, `read_vertex_normals`, etc.

### `Cast_Ray`
- Purpose: Tests ray collision against the mesh.
- Calls: `cast_ray_brute_force`, `cast_semi_infinite_axis_aligned_ray`.

### `Cast_World_Space_AABox`
- Purpose: Tests axis-aligned box collision in world space.
- Calls: `cast_aabox_identity`, `cast_aabox_z90`, etc.

### `Generate_Culling_Tree`
- Purpose: Generates a culling tree for optimization.
- Calls: None (internal logic).

## Globals
- **OPTIMIZE_PLANEEQ_RAM (Define)**: Controls plane equation memory optimization.
- **OPTIMIZE_VNORM_RAM (Define)**: Controls vertex normal memory optimization.

## Dependencies
- Key includes: `always.h`, `refcount.h`, `simplevec.h`, `vector3.h`, `wwdebug.h`.
- External symbols: `AABoxClass`, `OBBoxClass`, `SphereClass`, `ChunkLoadClass`, `AABTreeClass`.
