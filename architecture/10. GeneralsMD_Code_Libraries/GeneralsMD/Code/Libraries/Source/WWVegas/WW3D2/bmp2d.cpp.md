# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bmp2d.cpp

## Purpose
Implements the `Bitmap2DObjClass` for rendering 2D bitmaps in the game engine, supporting various rendering modes and texture handling.

## Responsibilities
- Loads and renders 2D bitmaps from files or existing textures
- Handles texture splitting into power-of-two chunks for compatibility
- Configures shaders for additive, alpha, or opaque rendering
- Supports colorization and screen positioning options
- Manages vertex and texture data for 2D rendering

## Key Types
- `Bitmap2DObjClass` (Class): Main class for 2D bitmap rendering objects
- `ShaderClass` (Class): Used for configuring rendering shaders
- `VertexMaterialClass` (Class): Used for vertex material setup
- `TextureClass` (Class): Texture data container
- `SurfaceClass` (Class): Surface data container

## Key Functions
### `Bitmap2DObjClass(const char *filename, ...)`
- Purpose: Constructs a 2D bitmap from a file
- Calls: `WW3DAssetManager::Get_Instance()`, `TextureLoader::Request_Foreground_Loading()`, `SurfaceClass::Get_Description()`, `Find_POT()`, `NEW_REF()`, `Set_Shader()`, `Begin_Tri_Strip()`, `Vertex()`, `End_Tri_Strip()`

### `Bitmap2DObjClass(TextureClass *texture, ...)`
- Purpose: Constructs a 2D bitmap from an existing texture
- Calls: `WW3D::Get_Device_Resolution()`, `TextureLoader::Request_Foreground_Loading()`, `Set_Shader()`, `Begin_Tri_Strip()`, `Vertex()`, `End_Tri_Strip()`

### `Clone()`
- Purpose: Creates a copy of the bitmap object
- Calls: `NEW_REF()`

## Globals
None

## Dependencies
- `bmp2d.h`, `pot.h`, `ww3d.h`, `texture.h`, `surfaceclass.h`, `assetmgr.h`, `textureloader.h`, `ww3dformat.h`
- `WW3DAssetManager`, `TextureLoader`, `ShaderClass`, `VertexMaterialClass`, `TextureClass`, `SurfaceClass`, `DynamicScreenMeshClass`
