# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DVideoBuffer.cpp

## Purpose
Implements a video buffer class for the W3D rendering engine, managing texture allocation and surface locking.

## Responsibilities
- Allocates and manages texture memory for video buffers
- Handles surface locking/unlocking for pixel access
- Converts between VideoBuffer and W3D format types
- Cleans up resources when buffers are freed

## Key Types
- `W3DVideoBuffer` (Class): Video buffer implementation for W3D engine
- `TextureClass` (Class): W3D texture object wrapper
- `SurfaceClass` (Class): W3D surface object wrapper

## Key Functions
### `allocate`
- Purpose: Allocates a texture buffer of specified dimensions
- Calls: `free()`, `TextureLoader::Validate_Texture_Size()`, `TextureClass` constructor, `lock()`, `unlock()`

### `lock`
- Purpose: Locks the surface for pixel access and returns memory pointer
- Calls: `unlock()`, `Get_Surface_Level()`, `Lock()`

### `unlock`
- Purpose: Unlocks the surface after pixel access
- Calls: `Unlock()`, `Release_Ref()`

### `TypeToW3DFormat`
- Purpose: Converts VideoBuffer format types to W3D format types
- Calls: None

### `W3DFormatToType`
- Purpose: Converts W3D format types to VideoBuffer format types
- Calls: None

## Globals
- None

## Dependencies
- `Common/GameMemory.h`
- `WW3D2/texture.h`
- `WW3D2/textureloader.h`
- `W3DDevice/GameClient/W3DVideoBuffer.h`
- `TextureClass`, `SurfaceClass` from W3D engine
- `VideoBuffer` base class
