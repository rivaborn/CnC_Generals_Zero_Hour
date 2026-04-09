# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdcubemap.h

## Purpose
Defines classes for cube map shaders in the WWSHADE rendering system.

## Responsibilities
- Declares `ShdCubeMapDefClass` for cube map shader definitions
- Declares `Shd6CubeMapClass` for cube map shader implementation
- Provides interface for texture-based lighting effects
- Manages shader creation and rendering parameters

## Key Types
- **ShdCubeMapDefClass (Class)**: Cube map shader definition with texture and lighting parameters
- **Shd6CubeMapClass (Class)**: Cube map shader implementation for rendering
- **None**: No enums/structs defined

## Key Functions
### ShdCubeMapDefClass::Create
- Purpose: Creates a shader instance from the definition
- Calls: Not inferable

### Shd6CubeMapClass::Apply_Shared
- Purpose: Applies shared shader state for cube map rendering
- Calls: Not inferable

### Shd6CubeMapClass::Apply_Instance
- Purpose: Applies instance-specific shader state for cube map rendering
- Calls: Not inferable

## Globals
- **View_Projection_Matrix (Matrix4x4)**: Static matrix for cube map projection

## Dependencies
- `shdinterface.h`, `shddef.h`, `saveload.h`, `shader.h`
- `ShdDefClass`, `ShdInterfaceClass`, `TextureClass`, `Vector3`, `Vector4`, `Matrix4x4`, `D3DMATERIAL8`
