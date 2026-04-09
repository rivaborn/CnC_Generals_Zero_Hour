# Generals/Code/Libraries/Source/WWVegas/WW3D2/mapper.cpp

## Purpose
Implements texture mapping effects for the SAGE engine, including animation, distortion, and environment mapping.

## Responsibilities
- Defines texture mapper classes for various effects (linear offset, scale, grid, rotation, sine, environment, etc.)
- Manages texture coordinate transformations via Direct3D texture matrices
- Provides utility functions for resetting texture mappers
- Handles time-based animation of texture coordinates

## Key Types
- **TextureMapperClass (Class)**: Base class for texture mapping effects
- **LinearOffsetTextureMapperClass (Class)**: Implements scrolling textures
- **ScaleTextureMapperClass (Class)**: Handles texture scaling
- **GridTextureMapperClass (Class)**: Manages grid-based texture animation
- **RotateTextureMapperClass (Class)**: Implements rotating textures
- **EnvironmentMapperClass (Class)**: Handles environment/cube mapping
- **EdgeMapperClass (Class)**: Specialized edge mapping effect
- **Matrix3D (Struct)**: 3x4 transformation matrix
- **Vector2/Vector3/Vector4 (Structs)**: Math vectors

## Key Functions
### F2DW
- Purpose: Converts float to DWORD via pointer casting
- Calls: None

### Reset_All_Texture_Mappers
- Purpose: Recursively resets all texture mappers in a render object hierarchy
- Calls: WW3D::Get_Sync_Time(), MeshClass::Make_Unique(), MaterialInfoClass::Reset_Texture_Mappers()

## Globals
- None

## Dependencies
- Key includes: mapper.h, ww3d.h, ini.h, chunkio.h, w3derr.h, meshmatdesc.h, dx8wrapper.h, wwdebug.h, matinfo.h, rendobj.h, mesh.h
- External symbols: WW3D::Get_Sync_Time(), DX8Wrapper::Set_Transform(), DX8Wrapper::Set_DX8_Texture_Stage_State(), WWMath::Floor(), WWMath::Cos(), WWMath::Sin(), etc.
