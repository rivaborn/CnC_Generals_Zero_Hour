# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdmesh.cpp

## Purpose
Handles shader-based mesh rendering and collision detection in the SAGE engine.

## Responsibilities
- Manages sub-meshes and their renderers
- Handles rendering with lighting and shadow effects
- Implements collision detection (ray, box, OBBox)
- Loads W3D mesh data and initializes from legacy meshes
- Maintains bounding volume calculations

## Key Types
- **ShdMeshClass (Class)**: Main mesh class handling rendering and collision
- **ShdSubMeshClass (Class)**: Sub-mesh container (referenced)
- **ShdRendererClass (Class)**: Renderer instance (referenced)
- **W3dShdMeshHeaderStruct (Struct)**: W3D file header structure

## Key Functions
### `Render`
- Purpose: Renders the mesh with lighting/shadow effects
- Calls: `Set_Lighting_Environment`, `ShdRendererClass::Render`

### `Cast_Ray`
- Purpose: Tests ray intersection with mesh
- Calls: `Matrix3D::Rotate_Vector`, `Matrix3D::Transform_Vector`

### `Cast_AABox`
- Purpose: Tests axis-aligned box collision
- Calls: `MeshGeometryClass::Cast_World_Space_AABox`

### `Load_W3D`
- Purpose: Loads mesh data from W3D file format
- Calls: `ShdSubMeshClass::Load_W3D`, `WWDEBUG_SAY`

### `Update_Cached_Bounding_Volumes`
- Purpose: Updates collision bounding volumes
- Calls: `Get_Obj_Space_Bounding_Sphere`, `Get_Obj_Space_Bounding_Box`

## Globals
- **LightEnvironment (LightEnvironmentClass*)**: Current lighting environment
- **Applying_Shadow_Map (bool)**: Shadow map application flag

## Dependencies
- Key includes: `shdmesh.h`, `shdsubmesh.h`, `shdrenderer.h`, `rinfo.h`, `camera.h`
- External symbols: `WWPROFILE`, `DX8_RECORD_MESH_RENDER`, `CollisionMath::Overlap_Test`
