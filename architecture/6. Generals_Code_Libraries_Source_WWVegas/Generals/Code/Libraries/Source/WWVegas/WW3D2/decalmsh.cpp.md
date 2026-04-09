# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.cpp

## Purpose
Implements decal mesh rendering for the SAGE engine, handling both rigid and skinned decals.

## Responsibilities
- Manages `DecalPolyClass` for polygon clipping
- Implements `RigidDecalMeshClass` for static decals
- Implements `SkinDecalMeshClass` for animated/skinned decals
- Handles decal creation, deletion, and rendering
- Processes material runs for efficient rendering

## Key Types
- **DecalPolyClass (Class)**: Temporary polygon clipping utility
- **DecalMeshClass (Class)**: Base class for decal meshes
- **RigidDecalMeshClass (Class)**: Decal mesh for static geometry
- **SkinDecalMeshClass (Class)**: Decal mesh for skinned/animated geometry

## Key Functions
### DecalPolyClass::Clip
- Purpose: Clips polygon against a plane
- Calls: `PlaneClass::In_Front`, `PlaneClass::Compute_Intersection`, `Vector3::Lerp`

### RigidDecalMeshClass::Render
- Purpose: Renders all decals in the mesh
- Calls: `DX8Wrapper::Set_Transform`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Draw_Triangles`

### SkinDecalMeshClass::Render
- Purpose: Renders skinned decals using deformed vertices
- Calls: `Parent->Get_Deformed_Vertices`, `DX8Wrapper::Set_Transform`, `DX8Wrapper::Draw_Triangles`

## Globals
- `_DecalPoly0 (DecalPolyClass)`: Temporary clipping polygon storage
- `_DecalPoly1 (DecalPolyClass)`: Temporary clipping polygon storage
- `_TempVertexBuffer (SimpleDynVecClass<Vector3>)`: Temporary vertex storage for skin decals
- `_TempNormalBuffer (SimpleDynVecClass<Vector3>)`: Temporary normal storage for skin decals

## Dependencies
- `decalmsh.h`, `decalsys.h`, `mesh.h`, `meshmdl.h`, `plane.h`
- `statistics.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`
- `simplevec.h`, `texture.h`, `dx8wrapper.h`
- `Vector3`, `Vector3i`, `Matrix3D`, `MaterialPassClass`
