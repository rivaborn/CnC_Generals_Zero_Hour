# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DVideoBuffer.cpp

## Purpose
Implements a video buffer class for the W3D rendering engine, managing texture allocation and surface locking.

## Responsibilities
- Allocates and manages texture memory for video buffers
- Handles surface locking/unlocking for pixel access
- Converts between VideoBuffer and W3D format types
- Cleans up resources on destruction

## Key Types
- W3DVideoBuffer (Class): Wraps a texture for video buffer operations
- TextureClass (Class): Underlying texture object (external)
- SurfaceClass (Class): Surface object for pixel access (external)

## Key Functions
### allocate
- Purpose: Allocates texture memory for the video buffer
- Calls: free(), TextureLoader::Validate_Texture_Size(), TextureClass constructor, lock(), unlock()

### lock
- Purpose: Locks the surface for pixel access and returns a pointer to the pixel data
- Calls: unlock(), Get_Surface_Level(), Lock()

### unlock
- Purpose: Unlocks the surface after pixel access
- Calls: Unlock(), Release_Ref()

### free
- Purpose: Releases all allocated resources
- Calls: unlock(), Release_Ref(), VideoBuffer::free()

### TypeToW3DFormat
- Purpose: Converts VideoBuffer::Type to WW3DFormat
- Calls: None

### W3DFormatToType
- Purpose: Converts WW3DFormat to VideoBuffer::Type
- Calls: None

## Globals
None

## Dependencies
- Common/GameMemory.h
- WW3D2/texture.h
- WW3D2/textureloader.h
- W3DDevice/GameClient/W3DVideoBuffer.h
- VideoBuffer base class
- TextureClass, SurfaceClass from WW3D2
