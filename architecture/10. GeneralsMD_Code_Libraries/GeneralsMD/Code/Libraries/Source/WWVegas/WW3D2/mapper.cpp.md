# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mapper.cpp

## Purpose
Implements texture mapping effects for the SAGE engine, including scaling, rotation, animation, and environment mapping.

## Responsibilities
- Defines various texture mapper classes (scale, offset, grid, rotation, etc.)
- Manages texture coordinate transformations via Direct3D texture matrices
- Handles time-based animation of texture coordinates
- Provides utility functions for resetting texture mappers

## Key Types
- **TextureMapperClass (Class)**: Base class for texture mappers
- **ScaleTextureMapperClass (Class)**: Scales texture coordinates
- **LinearOffsetTextureMapperClass (Class)**: Animates texture offset linearly
- **GridTextureMapperClass (Class)**: Animates textures in a grid pattern
- **RotateTextureMapperClass (Class)**: Rotates textures over time
- **RandomTextureMapperClass (Class)**: Randomly animates textures
- **BumpEnvTextureMapperClass (Class)**: Adds bump mapping with environment effects
- **GridWSEnvMapperClass (Class)**: Grid mapping in world space with environment effects
- **Random4Class (Class)**: Random number generator utility

## Key Functions
### F2DW
- Purpose: Converts float to DWORD
- Calls: None

### Reset_All_Texture_Mappers
- Purpose: Recursively resets all texture mappers in a render object
- Calls: WW3D::Get_Sync_Time(), DX8Wrapper functions

## Globals
- **rand4 (Random4Class)**: Global random number generator instance

## Dependencies
- Key includes: mapper.h, ww3d.h, ini.h, chunkio.h, w3derr.h, meshmatdesc.h, dx8wrapper.h, wwdebug.h, matinfo.h, rendobj.h, mesh.h, random.h, bound.h
- External symbols: WW3D, DX8Wrapper, WWMath, Matrix4x4, Vector2, Vector3, Vector4, INIClass, RenderObjClass, MeshClass, MaterialInfoClass
