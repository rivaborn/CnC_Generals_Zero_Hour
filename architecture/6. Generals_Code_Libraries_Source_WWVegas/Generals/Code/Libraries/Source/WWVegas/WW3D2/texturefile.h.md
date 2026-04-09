# Generals/Code/Libraries/Source/WWVegas/WW3D2/texturefile.h

## Purpose
Defines the `TextureFileClass`, the primary texture class in WW3D for managing texture loading, reduction, and rendering.

## Responsibilities
- Load and manage texture surfaces from files
- Handle texture reduction based on screen size and performance needs
- Provide statistics and debugging tools for texture management
- Support background loading of texture mipmaps

## Key Types
- **TextureFileClass (class)**: Main texture class handling file-based textures with optional reduction
- **TextureLoaderInfoStruct (struct)**: Internal structure for texture loader communication

## Key Functions
### `TextureFileClass(const char * filename)`
- Purpose: Constructor that initializes a texture from a file
- Calls: Not visible in header

### `getMipmapData(MultiRequest& m)`
- Purpose: Provides mipmap data for rendering
- Calls: `Fill_Multi_Request_From_Surface`

### `Request_Reduction(float reduction_factor)`
- Purpose: Requests a specific reduction factor for the texture
- Calls: Not visible in header

### `Process_Reduction(void)`
- Purpose: Adjusts current reduction factor if needed
- Calls: Not visible in header

### `Apply_New_Surface()`
- Purpose: Applies a new surface to the texture
- Calls: Not visible in header

## Globals
- **`_CurrentTimeStamp` (static unsigned int)**: Tracks frame timing for reduction processing
- **`_SwitchThreshold` (static float)**: Controls hysteresis for reduction switching

## Dependencies
- `srTexture.hpp` (DirectX texture interface)
- `always.h`, `classid.h`, `wwdebug.h`, `wwstring.h` (WW3D utilities)
- `srClassSupport`, `srTexture`, `FrameHandle`, `MultiRequest`, `srColorSurfaceIFace` (WW3D framework types)
