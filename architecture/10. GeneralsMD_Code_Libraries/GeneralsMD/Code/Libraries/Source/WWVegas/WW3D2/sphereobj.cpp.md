# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sphereobj.cpp

## Purpose
Implements sphere rendering functionality for the SAGE engine, including mesh generation, LOD management, and rendering.

## Responsibilities
- Manages sphere mesh generation and LOD arrays
- Handles sphere rendering with material/shader setup
- Provides collision detection (ray/sphere intersection)
- Supports animated spheres with color/alpha/scale channels
- Implements sphere visibility and rendering optimization

## Key Types
- **SphereRenderObjClass (Class)**: Main sphere rendering object with transform, material, and animation support
- **SphereMeshClass (Class)**: Geometry container for sphere meshes with vertex/strip/fan data
- **AlphaVectorStruct (Struct)**: Defines alpha vector properties (angle, intensity)
- **CHUNKID_SPHERE_DEF (Enum)**: Chunk ID for sphere definition data
- **CHUNKID_COLOR_CHANNEL (Enum)**: Chunk ID for color channel data

## Key Functions
### SphereRenderObjClass::Generate_Shared_Mesh_Arrays
- Purpose: Generates shared LOD mesh arrays for spheres
- Calls: SphereMeshClass::Generate, SphereMeshClass::Set_Alpha_Vector

### SphereMeshClass::Generate
- Purpose: Creates sphere geometry with vertices, normals, UVs, and primitive indices
- Calls: Matrix3x3::Make_Identity, Matrix3x3::Rotate_Z, Matrix3x3::Rotate_X

### SphereMeshClass::Set_Alpha_Vector
- Purpose: Applies alpha vector effect to sphere vertices for hole/gradient effects
- Calls: Vector3::Dot_Product

### SphereRenderObjClass::Init_Material
- Purpose: Sets up default material and shader for spheres
- Calls: VertexMaterialClass constructor, ShaderClass methods

## Globals
- **Sphere_Array_Valid (bool)**: Tracks if shared sphere mesh arrays are initialized
- **SphereMeshArray (SphereMeshClass[])**: Pre-generated sphere meshes at different LODs
- **SphereLODCosts (float[])**: Polygon counts for LOD selection
- **_SphereLoader (ChunkLoaderClass)**: Chunk loader for sphere definition files

## Dependencies
- Key includes: sphereobj.h, w3d_util.h, wwdebug.h, vertmaterial.h, ww3d.h
- External symbols: W3DNEWARRAY, REF_PTR_RELEASE, WW3DAssetManager, ShaderClass
- Math libraries: Matrix3x3, Vector3, Vector4
- Rendering: VertexMaterialClass, ShaderClass, DX8Wrapper, SortingRenderer
