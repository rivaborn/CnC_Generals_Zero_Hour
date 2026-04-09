# Generals/Code/Libraries/Source/WWVegas/WW3D2/bmp2d.cpp

## Purpose
Implements 2D bitmap rendering for the SAGE engine, supporting both file-based and texture-based bitmaps with various rendering options.

## Responsibilities
- Load and render 2D bitmaps from files or existing textures
- Handle texture tiling for large bitmaps using power-of-two textures
- Support additive, alpha, and opaque rendering modes
- Enable colorization of bitmaps via vertex materials
- Manage screen positioning and centering

## Key Types
- **Bitmap2DObjClass (Class)**: Main class for 2D bitmap rendering objects
- **SurfaceClass (External)**: Handles image surface data
- **TextureClass (External)**: Manages texture resources
- **ShaderClass (External)**: Defines rendering shaders
- **VertexMaterialClass (External)**: Controls vertex material properties

## Key Functions
### Bitmap2DObjClass(const char *filename, ...)
- Purpose: Constructs a 2D bitmap from a file
- Calls: `WW3D::Get_Device_Resolution`, `NEW_REF(SurfaceClass)`, `Find_POT`, `NEW_REF(TextureClass)`, `Set_Texture`, `Begin_Tri_Strip`, `Vertex`, `End_Tri_Strip`

### Bitmap2DObjClass(TextureClass *texture, ...)
- Purpose: Constructs a 2D bitmap from an existing texture
- Calls: `WW3D::Get_Device_Resolution`, `texture->Get_Level_Description`, `Set_Texture`, `Begin_Tri_Strip`, `Vertex`, `End_Tri_Strip`

### Clone()
- Purpose: Creates a copy of the bitmap object
- Calls: `NEW_REF(Bitmap2DObjClass)`

## Globals
None

## Dependencies
- `bmp2d.h`, `pot.h`, `ww3d.h`, `texture.h`, `surfaceclass.h`
- `WW3D`, `SurfaceClass`, `TextureClass`, `ShaderClass`, `VertexMaterialClass`, `DynamicScreenMeshClass`
