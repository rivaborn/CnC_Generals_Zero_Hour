# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texturefile.h

## Purpose
Defines the `TextureFileClass`, the primary texture class in WW3D for managing texture loading, reduction, and rendering.

## Responsibilities
- Load and manage texture surfaces from files
- Handle dynamic texture reduction based on screen size
- Provide performance statistics for texture memory usage
- Support debugging features like texture flashing

## Key Types
- **TextureFileClass (class)**: Main texture class handling loading, reduction, and rendering
- **TextureLoaderInfoStruct (struct)**: Internal structure for texture loader communication
- **FrameHandle (type)**: Handle to texture frame data

## Key Functions
### `TextureFileClass(const char * filename)`
- Purpose: Constructor that initializes texture from a file
- Calls: Not visible in header

### `getMipmapData(MultiRequest& m)`
- Purpose: Provides mipmap data for rendering
- Calls: `Fill_Multi_Request_From_Surface`

### `Request_Reduction(float reduction_factor)`
- Purpose: Requests a specific reduction factor for texture rendering
- Calls: None visible

### `Process_Reduction(void)`
- Purpose: Adjusts current reduction factor if needed during rendering
- Calls: None visible

### `Apply_New_Surface()`
- Purpose: Applies a new surface to the texture
- Calls: None visible

## Globals
- **_CurrentTimeStamp (static unsigned int)**: Tracks frame timing for reduction processing
- **_SwitchThreshold (static float)**: Controls hysteresis for reduction switching
- **LockedSurface (srColorSurfaceIFace**)**: Pointer to the locked surface (reduced texture)

## Dependencies
- `srTexture.hpp` (DirectX 8 texture interface)
- `always.h`, `classid.h`, `wwdebug.h`, `wwstring.h` (WW3D utilities)
- `srClassSupport`, `srTexture`, `FrameHandle` (WW3D base classes/interfaces)
