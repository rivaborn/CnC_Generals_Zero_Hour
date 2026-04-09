# Generals/Code/Libraries/Source/WWVegas/WW3D2/textureloader.cpp

## Purpose
Handles asynchronous texture loading and management for the SAGE engine, including DDS/TGA loading, mipmapping, and hardware format validation.

## Responsibilities
- Manages texture loading via a background thread
- Handles DDS/TGA texture loading with format conversion
- Validates texture sizes against hardware capabilities
- Provides thumbnail generation for textures
- Mainages texture task queues (load, deferred, finished, delete)

## Key Types
- **TextureLoadTaskClass (Class)**: Represents a texture loading task with state tracking
- **LoaderThreadClass (Class)**: Background thread for asynchronous texture loading
- **WW3DFormat (Enum)**: Texture format identifiers (DXT1/3/5, A8R8G8B8, etc.)

## Key Functions
### Is_Format_Compressed
- Purpose: Checks if a texture format is compressed and hardware-supported
- Calls: DX8Caps::Support_DXTC(), WW3D::Get_Texture_Compression_Mode()

### Load_Compressed_Texture
- Purpose: Loads DDS textures with optional reduction and mipmapping
- Calls: DDSFileClass methods, DX8Wrapper::_Create_DX8_Texture()

### TextureLoader::Load_Surface_Immediate
- Purpose: Synchronously loads a texture surface from TGA
- Calls: Targa methods, BitmapHandlerClass::Copy_Image(), DX8Wrapper::_Create_DX8_Surface()

### TextureLoadTaskClass::Begin_Texture_Load
- Purpose: Initiates texture loading (DDS or TGA path)
- Calls: DDSFileClass, Targa, TextureLoader::Validate_Texture_Size(), DX8Wrapper::_Create_DX8_Texture()

## Globals
- **LoadListHead (TextureLoadTaskClass*)**: Head of pending load tasks
- **DeferredListHead (TextureLoadTaskClass*)**: Head of deferred load tasks
- **FinishedListHead (TextureLoadTaskClass*)**: Head of completed tasks
- **ThumbnailListHead (TextureLoadTaskClass*)**: Head of thumbnail tasks
- **DeleteTaskListHead (TextureLoadTaskClass*)**: Head of tasks to delete
- **mutex (CriticalSectionClass)**: Thread synchronization mutex

## Dependencies
- Direct3D 8 (D3D8.h, D3dx8tex.h)
- Engine systems: DX8Wrapper, DX8Caps, WW3D
- File formats: Targa, DDSFileClass
- Memory: WWMemLog
- Threading: ThreadClass, CriticalSectionClass
- Utilities: BitmapHandlerClass, MissingTexture
