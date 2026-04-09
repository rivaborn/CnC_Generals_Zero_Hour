# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshmatdesc.cpp

## Purpose
Implements material and texture management for 3D meshes in the SAGE engine, handling vertex materials, UV coordinates, and rendering passes.

## Responsibilities
- Manages mesh material descriptions (MeshMatDescClass)
- Handles texture and vertex material buffers (TexBufferClass, MatBufferClass)
- Manages UV coordinate buffers (UVBufferClass)
- Provides material configuration and post-load processing

## Key Types
- **MatBufferClass (class)**: Manages shared buffers of VertexMaterialClass pointers
- **TexBufferClass (class)**: Manages shared buffers of TextureClass pointers
- **UVBufferClass (class)**: Manages UV coordinate arrays with CRC hashing
- **MeshMatDescClass (class)**: Core class for mesh material descriptions
- **ShaderClass (class)**: Represents shader configurations (external)

## Key Functions
### MatBufferClass::Set_Element
- Purpose: Sets a material pointer in the buffer with reference counting
- Calls: REF_PTR_SET

### MeshMatDescClass::Post_Load_Process
- Purpose: Configures materials and pre-multiplies vertex colors after loading
- Calls: Configure_Material, DX8Wrapper::Convert_Color, CRC_Memory

### MeshMatDescClass::Configure_Material
- Purpose: Configures a vertex material for a specific render pass
- Calls: VertexMaterialClass methods (Set_Diffuse_Color_Source, etc.)

### MeshMatDescClass::Install_UV_Array
- Purpose: Installs UV coordinates into the material description
- Calls: CRC_Memory, NEW_REF

## Globals
- **MeshMatDescClass::NullShader (ShaderClass)**: Marker for no shader data

## Dependencies
- Key includes: meshmatdesc.h, texture.h, vertmaterial.h, realcrc.h, dx8wrapper.h, dx8caps.h
- External symbols: REF_PTR_SET, REF_PTR_RELEASE, NEW_REF, CRC_Memory, DX8Wrapper, DX8Caps, WW3D
