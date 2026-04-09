# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshmatdesc.cpp

## Purpose
Manages mesh material descriptions, including textures, shaders, UV coordinates, and vertex materials for 3D rendering in the SAGE engine.

## Responsibilities
- Handles material buffer classes (MatBufferClass, TexBufferClass, UVBufferClass)
- Manages mesh material descriptions (MeshMatDescClass)
- Processes post-load material configurations
- Configures vertex materials and shaders
- Optimizes material arrays and UV coordinates

## Key Types
- **MatBufferClass (Class)**: Manages shared vertex material buffers
- **TexBufferClass (Class)**: Manages shared texture buffers
- **UVBufferClass (Class)**: Manages UV coordinate buffers with CRC comparison
- **MeshMatDescClass (Class)**: Core class for mesh material descriptions
- **ShaderClass (Class)**: Represents shader configurations (external)

## Key Functions
### `MeshMatDescClass::Post_Load_Process`
- Purpose: Configures materials after loading, including lighting and color processing
- Calls: `Configure_Material`, `DX8Wrapper::Convert_Color`, `Peek_Material`

### `MeshMatDescClass::Configure_Material`
- Purpose: Sets up material sources for UV coordinates and colors
- Calls: None (direct property access)

### `MeshMatDescClass::Install_UV_Array`
- Purpose: Installs UV coordinates into the material description
- Calls: `CRC_Memory`, `Set_UV_Source`

### `MeshMatDescClass::Do_Mappers_Need_Normals`
- Purpose: Checks if any material mappers require normals
- Calls: `Material->Do_Mappers_Need_Normals`, `Peek_Material`

## Globals
- **MeshMatDescClass::NullShader (ShaderClass)**: Marker for no shader data

## Dependencies
- `meshmatdesc.h`, `texture.h`, `vertmaterial.h`, `realcrc.h`, `dx8wrapper.h`, `dx8caps.h`, `meshmdl.h`
- External symbols: `DX8Wrapper`, `WW3D`, `Vector2`, `Vector3`, `Vector4`, `ShareBufferClass`, `NEW_REF`, `REF_PTR_SET`, `REF_PTR_RELEASE`, `WWASSERT`
