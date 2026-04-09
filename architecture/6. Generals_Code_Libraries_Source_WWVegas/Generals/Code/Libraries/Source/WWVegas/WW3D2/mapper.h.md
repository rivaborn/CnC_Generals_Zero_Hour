# Generals/Code/Libraries/Source/WWVegas/WW3D2/mapper.h

## Purpose
Defines texture mapping classes for the W3D rendering engine, handling UV coordinate transformations.

## Responsibilities
- Declares base `TextureMapperClass` and derived mappers (scale, rotation, environment, etc.)
- Defines mapper IDs for identification
- Provides utility function to reset all texture mappers

## Key Types
- **TextureMapperClass (Class)**: Base class for texture mappers with common interface
- **ScaleTextureMapperClass (Class)**: Scales UV coordinates
- **LinearOffsetTextureMapperClass (Class)**: Applies linear offset to UVs over time
- **GridTextureMapperClass (Class)**: Animates textures via grid offsets
- **RotateTextureMapperClass (Class)**: Rotates texture coordinates
- **EnvironmentMapperClass (Class)**: Maps textures based on normals
- **ScreenMapperClass (Class)**: Maps textures using screen coordinates
- **RandomTextureMapperClass (Class)**: Randomly modifies texture coordinates
- **BumpEnvTextureMapperClass (Class)**: Handles bump mapping with time-based transforms
- **MAPPER_ID_* (Enum)**: Enumerates mapper types

## Key Functions
### Reset_All_Texture_Mappers
- Purpose: Resets all texture mappers for a render object
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `refcount.h`, `w3d_file.h`, `w3derr.h`, `wwdebug.h`, `vector2.h`, `vector3.h`, `ww3d.h`
- `INIClass` (forward declaration)
- `W3DMPO`, `RefCountClass` (base classes)
