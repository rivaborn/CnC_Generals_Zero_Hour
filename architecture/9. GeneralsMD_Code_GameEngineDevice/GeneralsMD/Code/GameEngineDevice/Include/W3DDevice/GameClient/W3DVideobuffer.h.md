# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DVideobuffer.h

## Purpose
Defines the W3DVideoBuffer class, a video buffer interface for W3D TextureClass.

## Responsibilities
- Manages video buffer allocation and deallocation
- Provides access to buffer memory via lock/unlock
- Wraps W3D texture and surface objects
- Converts between VideoBuffer::Type and WW3DFormat

## Key Types
- **W3DVideoBuffer (Class)**: Video buffer interface for W3D textures
- **TextureClass (Class)**: W3D texture object (forward reference)
- **SurfaceClass (Class)**: W3D surface object (forward reference)

## Key Functions
### W3DVideoBuffer(Type format)
- Purpose: Constructor for W3DVideoBuffer.
- Calls: Not inferable.

### allocate(UnsignedInt width, UnsignedInt height)
- Purpose: Allocates a video buffer of specified dimensions.
- Calls: Not inferable.

### free()
- Purpose: Frees the allocated video buffer.
- Calls: Not inferable.

### lock()
- Purpose: Returns a pointer to the start of the buffer memory.
- Calls: Not inferable.

### unlock()
- Purpose: Releases the buffer after locking.
- Calls: Not inferable.

### valid()
- Purpose: Checks if the buffer is valid for use.
- Calls: Not inferable.

### TypeToW3DFormat(VideoBuffer::Type format)
- Purpose: Converts VideoBuffer::Type to WW3DFormat.
- Calls: Not inferable.

### W3DFormatToType(WW3DFormat w3dFormat)
- Purpose: Converts WW3DFormat to VideoBuffer::Type.
- Calls: Not inferable.

## Globals
None

## Dependencies
