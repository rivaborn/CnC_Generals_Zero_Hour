# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mapper.h

## Purpose
Defines texture mapping classes for the W3D rendering engine, including various mapper types for UV coordinate manipulation.

## Responsibilities
- Declares base `TextureMapperClass` and derived classes for different mapping techniques
- Defines mapper IDs for identification
- Provides utility functions for texture mapper management
- Supports time-variant and static texture mappings

## Key Types
- `TextureMapperClass` (Class): Base class for all texture mappers
- `ScaleTextureMapperClass` (Class): Scales UV coordinates
- `LinearOffsetTextureMapperClass` (Class): Applies linear offset to UVs
- `GridTextureMapperClass` (Class): Animates textures via grid offsets
- `RotateTextureMapperClass` (Class): Rotates texture coordinates
- `EnvironmentMapperClass` (Class): Maps textures based on normals
- `ScreenMapperClass` (Class): Maps textures based on screen coordinates
- `RandomTextureMapperClass` (Class): Randomly modifies texture coordinates
- `BumpEnvTextureMapperClass` (Class): Modifies bump map transforms
- `AxisType` (Enum): Defines axis types (X, Y, Z)

## Key Functions
### `Reset_All_Texture_Mappers`
- Purpose: Resets all texture mappers for a render object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `refcount.h`, `w3d_file.h`, `w3derr.h`, `wwdebug.h`, `vector2.h`, `vector3.h`, `ww3d.h`, `matrix4.h`
- `INIClass`, `W3DMPO`, `RefCountClass`, `RenderObjClass`
