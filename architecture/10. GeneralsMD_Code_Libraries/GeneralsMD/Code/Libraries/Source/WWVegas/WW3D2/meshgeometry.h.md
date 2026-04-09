# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.h

## Purpose
Defines the `MeshGeometryClass` for handling 3D mesh geometry data, including vertices, polygons, normals, and collision detection.

## Responsibilities
- Manages mesh geometry data (vertices, polygons, normals, etc.)
- Provides collision detection and intersection tests
- Handles W3D file format loading for mesh data
- Supports skinning and deformation for animated meshes
- Maintains bounding volumes and culling structures

## Key Types
- **MeshGeometryClass (Class)**: Core class for mesh geometry data and operations.
- **TriIndex (Class)**: Represents triangle indices (16-bit or 32-bit vectors).
- **FlagsType (Enum)**: Bit flags for mesh properties (dirty flags, rendering hints, etc.).

## Key Functions
### `Reset_Geometry(int polycount, int vertcount)`
- Purpose: Resets mesh geometry with specified polygon and vertex counts.
- Calls: Not inferable.

### `Compute_Plane_Equations(Vector4 * array)`
- Purpose: Computes plane equations for mesh polygons.
- Calls: Not inferable.

### `Compute_Vertex_Normals(Vector3 * array)`
- Purpose: Computes vertex normals for the mesh.
- Calls: Not inferable.

### `Cast_Ray(RayCollisionTestClass & raytest)`
- Purpose: Performs ray-casting against the mesh.
- Calls: `cast_ray_brute_force`, `cast_semi_infinite_axis_aligned_ray`.

### `Cast_AABox(AABoxCollisionTestClass & boxtest)`
- Purpose: Tests axis-aligned box collision with the mesh.
- Calls: `cast_aabox_identity`, `cast_aabox_z90`, `cast_aabox_z180`, `cast_aabox_z270`, `cast_aabox_brute_force`.

## Globals
- **OPTIMIZE_PLANEEQ_RAM (Define)**: Controls memory optimization for plane equations.
- **OPTIMIZE_VNORM_RAM (Define)**: Controls memory optimization for vertex normals.

## Dependencies
- Key includes: `always.h`, `refcount.h`, `bittype.h`, `simplevec.h`, `sharebuf.h`, `w3derr.h`, `vector3.h`, `vector3i.h`, `vector4.h`, `wwdebug.h`, `multilist.h`, `coltest.h`, `inttest.h`.
- External symbols: `AABoxClass`, `OBBoxClass`, `SphereClass`, `ChunkLoadClass`, `AABTreeClass`, `HTreeClass`, `RenderInfoClass`, `RayCollisionTestClass`, `AABoxCollisionTest
