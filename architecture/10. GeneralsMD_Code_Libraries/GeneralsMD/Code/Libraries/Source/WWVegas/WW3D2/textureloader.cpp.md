# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textureloader.cpp

## Purpose
Handles asynchronous texture loading for the SAGE engine, managing compressed/uncompressed textures, cube maps, and volume textures.

## Responsibilities
- Manages foreground/background texture loading queues
- Handles DDS/TGA texture loading and format conversion
- Validates texture dimensions against hardware capabilities
- Provides thread-safe texture loading via a dedicated loader thread
- Manages texture task pools and synchronization

## Key Types
- **TextureLoadTaskListClass (Class)**: Doubly-linked list for texture load tasks
- **SynchronizedTextureLoadTaskListClass (Class)**: Thread-safe wrapper for TextureLoadTaskListClass
- **LoaderThreadClass (Class)**: Background thread for asynchronous texture loading
- **TextureLoadTaskClass (Class)**: Base class for texture loading tasks (not shown in snippet)
- **CubeTextureLoadTaskClass (Class)**: Task for cube map textures
- **VolumeTextureLoadTaskClass (Class)**: Task for volume textures

## Key Functions
### Load_Compressed_Texture
- Purpose: Loads a compressed texture from DDS file
- Calls: DDSFileClass methods, DX8Wrapper::_Create_DX8_Texture

### Is_Format_Compressed
- Purpose: Checks if a texture format is compressed and supported
- Calls: DX8Wrapper::Get_Current_Caps()->Support_DXTC()

### Get_Texture_Information
- Purpose: Retrieves texture dimensions, format, and mip levels
- Calls: DDSFileClass and TargaFileClass methods

## Globals
- **_ForegroundCriticalSection (FastCriticalSectionClass)**: Synchronization for foreground queue
- **_BackgroundCriticalSection (FastCriticalSectionClass)**: Synchronization for background queue
- **_ForegroundQueue (SynchronizedTextureLoadTaskListClass)**: Queue for high-priority loads
- **_BackgroundQueue (SynchronizedTextureLoadTaskListClass)**: Queue for low-priority loads
- **_TexLoadFreeList (TextureLoadTaskListClass)**: Pool of reusable texture load tasks
- **_CubeTexLoadFreeList (TextureLoadTaskListClass)**: Pool for cube map tasks
- **_VolTexLoadFreeList (TextureLoadTaskListClass)**: Pool for volume texture tasks
- **_TextureLoadThread (LoaderThreadClass)**: Background thread for texture loading

## Dependencies
- Direct3D 8 (D3DX8tex.h)
- WW3D engine components (texture.h, ww3d.h)
- Threading utilities (mutex.h, thread.h)
- File handling (bufffile.h, ddsfile.h, targa.h)
- Asset management (assetmgr.h)
- Debug utilities (wwdebug.h)
