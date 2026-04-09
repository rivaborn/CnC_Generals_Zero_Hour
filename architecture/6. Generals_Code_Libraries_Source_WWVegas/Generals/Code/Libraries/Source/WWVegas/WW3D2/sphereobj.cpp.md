# Generals/Code/Libraries/Source/WWVegas/WW3D2/sphereobj.cpp

## Purpose
Implements sphere rendering functionality in the SAGE engine, including mesh generation, rendering, and collision detection.

## Responsibilities
- Manages sphere mesh generation and LOD (Level of Detail) arrays
- Handles sphere rendering with materials, textures, and shaders
- Provides collision detection (ray/sphere, sphere/sphere)
- Supports animated spheres with color/alpha/scale channels
- Maintains object-space bounding spheres

## Key Types
- **SphereRenderObjClass (Class)**: Main sphere rendering object with transform, material, and animation support
- **SphereMeshClass (Class)**: Handles sphere geometry generation (vertices, normals, UVs, strips, fans)
- **AlphaVectorStruct (Struct)**: Defines alpha vector for hole effects (direction + intensity)
- **CHUNKID_SPHERE_DEF/CHUNKID_COLOR_CHANNEL/etc (Enum)**: Chunk IDs for serialization

## Key Functions
### Generate_Shared_Mesh_Arrays
- Purpose: Creates shared LOD sphere mesh arrays
- Calls: None (static initialization)

### Init_Material
- Purpose: Sets up default material and shader for spheres
- Calls: VertexMaterialClass methods

### render_Sphere
- Purpose: Submits sphere geometry to the rendering pipeline
- Calls: WW3D::Render_Object, SphereMeshArray methods

### Cast_Ray
- Purpose: Performs ray-sphere intersection test
- Calls: Vector3::Dot_Product, WWMath functions

### Set_Alpha_Vector
- Purpose: Configures alpha hole effect using a direction vector
- Calls: Vector3::Dot_Product, Set_DCG

## Globals
- **Sphere_Array_Valid (bool)**: Tracks if shared mesh arrays are initialized
- **SphereMeshArray (SphereMeshClass[6])**: Pre-generated LOD sphere meshes
- **_SphereLoader (ChunkLoaderClass)**: Handles sphere object serialization

## Dependencies
- Key includes: sphereobj.h, w3d_util.h, chunkio.h, wwmath.h, assetmgr.h
- External symbols: WW3DAssetManager, ShaderClass, VertexMaterialClass, WWMath functions
