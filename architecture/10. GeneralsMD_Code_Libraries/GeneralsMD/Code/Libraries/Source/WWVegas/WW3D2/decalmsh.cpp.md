# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.cpp

## Purpose
Implements decal mesh rendering for the SAGE engine, handling both rigid and skinned meshes.

## Responsibilities
- Manages decal polygon clipping and rendering
- Handles dynamic vertex buffers for decal geometry
- Processes material runs for efficient rendering
- Supports both rigid and skinned mesh decals
- Manages decal creation/deletion lifecycle

## Key Types
- **DecalPolyClass (Class)**: Helper class for polygon clipping operations
- **DecalMeshClass (Class)**: Base class for decal mesh functionality
- **RigidDecalMeshClass (Class)**: Decal mesh for rigid (static) geometry
- **SkinDecalMeshClass (Class)**: Decal mesh for skinned (animated) geometry

## Key Functions
### DecalPolyClass::Clip
- Purpose: Clips a polygon against a plane
- Calls: `Reset`, `Add_Vertex`, `PlaneClass::In_Front`, `PlaneClass::Compute_Intersection`, `Vector3::Lerp`

### RigidDecalMeshClass::Render
- Purpose: Renders all decals on a rigid mesh
- Calls: `DX8Wrapper::Set_Transform`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Material`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Draw_Triangles`, `Process_Material_Run`

### SkinDecalMeshClass::Render
- Purpose: Renders all decals on a skinned mesh
- Calls: `DX8Wrapper::Set_Transform`, `MeshClass::Get_Deformed_Vertices`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Material`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Draw_Triangles`, `Process_Material_Run`

### SkinDecalMeshClass::Create_Decal
- Purpose: Generates a new decal on a skinned mesh
- Calls: `DecalGeneratorClass::Get_Decal_ID`, `DecalGeneratorClass::Set_Mesh_Transform`, `DecalGeneratorClass::Compute_Texture_Coordinate`, `DecalGeneratorClass::Add_Mesh`, `MaterialPassClass::Release_Ref`

## Globals
- `_DecalPoly0 (DecalPolyClass)`: Temporary clipping polygon storage
- `_DecalPoly1 (DecalPolyClass)`: Temporary clipping polygon storage
- `_TempVertexBuffer (SimpleDynVecClass<Vector3>)`: Temporary vertex storage for skinned meshes
- `_TempNormalBuffer (SimpleDynVecClass<Vector3>)`: Temporary normal storage for skinned meshes

## Dependencies
- `decalmsh.h`, `decalsys.h`, `rinfo.h`, `mesh.h`, `meshmdl.h`, `plane.h`, `statistics.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `simplevec.h`, `texture.h`, `dx8wrapper.h`, `dx8caps.h`
- `DX8Wrapper`, `Matrix3D`, `Vector3`, `PlaneClass`, `MeshClass`, `MeshModelClass`, `DecalSystemClass`, `DecalGeneratorClass`, `MaterialPassClass`
