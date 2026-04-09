# Generals/Code/Tools/WW3D/max2w3d/meshsave.cpp

## Purpose
Handles exporting 3D meshes from 3ds Max to the W3D format used by Command & Conquer Generals.

## Responsibilities
- Processes MAX mesh data and converts it to W3D format
- Computes mesh attributes, materials, and physical properties
- Handles vertex transformations and bounding volume calculations
- Manages material textures and shaders for export

## Key Types
- **MeshSaveClass** (Class): Main class handling mesh export logic
- **W3dMaterialDescClass** (Class): Material description container
- **W3dMaterialClass** (Class): Individual material representation
- **W3dVertexMaterialStruct** (Struct): Vertex material data structure
- **W3dShaderStruct** (Struct): Shader configuration structure

## Key Functions
### Compute_3x3_Determinant
- Purpose: Calculates determinant of 3x3 matrix portion
- Calls: None

### use_simple_rendering
- Purpose: Determines if mesh should use simplified rendering
- Calls: None

### setup_mesh_attributes
- Purpose: Builds bitfield of W3D mesh attributes
- Calls: Is_Collision_AABox, Is_Collision_OBBox, Is_Skin, Is_Camera_Aligned_Mesh, Is_Camera_Oriented_Mesh, Is_Physical_Collision, Is_Projectile_Collision, Is_Vis_Collision, Is_Camera_Collision, Is_Vehicle_Collision, Is_Hidden, Is_Two_Sided, Is_Shadow, Is_Shatterable, Is_NPatchable

### getMaterialUV
- Purpose: Retrieves material UV coordinates
- Calls: Not inferable

### isTexturedMaterial
- Purpose: Checks if material uses textures
- Calls: Mtl::GetSubTexmap, GameMtl::Get_Pass_Count, GameMtl::Get_Texture_Enable, GameMtl::Get_Texture

## Globals
- **_string1** (char[512]): Temporary string buffer
- **VOXEL_RESOLUTION** (const int): Resolution for physical property calculations

## Dependencies
- Max.h, stdmat.h, modstack.h, gamemtl.h, errclass.h, vxl.h, vxldbg.h, nodelist.h, hiersave.h, util.h, w3dappdata.h, skin.h, skindata.h, meshbuild.h, alphamodifier.h, aabtreebuilder.h, exportlog.h
- W3D-specific types and functions (W3dMaterialDescClass, W3dMaterialClass, etc.)
- 3ds Max SDK classes (INode, Mesh, Mtl, etc.)
