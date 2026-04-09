# Generals/Code/Libraries/Source/WWVegas/WW3D2/texturethumbnail.cpp

## Purpose
Manages texture thumbnails for the game, supporting loading from DDS/TGA files and caching them in memory.

## Responsibilities
- Load and cache texture thumbnails from DDS or TGA files
- Manage thumbnail instances via a hash table
- Initialize/deinitialize thumbnail system with optional disk persistence
- Handle texture format conversion and mipmap generation

## Key Types
- `ThumbnailClass` (Class): Represents a texture thumbnail with bitmap data and metadata
- `thumbnail_hash` (HashTemplateClass): Global hash table mapping filenames to ThumbnailClass instances

## Key Functions
### `ThumbnailClass::ThumbnailClass(const StringClass& filename)`
- Purpose: Loads a thumbnail from DDS or TGA file, converting to A8R8G8B8 format
- Calls: `DDSFileClass::Load`, `Targa::Open`, `BitmapHandlerClass::Copy_Image`

### `ThumbnailClass::Init()`
- Purpose: Initializes thumbnail system and loads cached thumbnails from disk (disabled in code)
- Calls: `file_auto_ptr` operations, `ThumbnailClass` constructor

### `ThumbnailClass::Deinit()`
- Purpose: Cleans up thumbnail system and optionally saves thumbnails to disk (disabled in code)
- Calls: `HashTemplateIterator` operations, `delete` on thumbnails

## Globals
- `thumbnail_hash` (HashTemplateClass): Maps filenames to ThumbnailClass instances
- `_ThumbHashModified` (bool): Tracks if hash table was modified
- `_ThumbnailMemory` (unsigned char*): Pointer to cached thumbnail memory
- `THUMBNAIL_FILENAME` (const char*): Path to thumbnail cache file

## Dependencies
- `texturethumbnail.h`, `hashtemplate.h`, `missingtexture.h`, `targa.h`, `ww3dformat.h`, `ddsfile.h`, `textureloader.h`, `bitmaphandler.h`, `ffactory.h`
- `W3DNEWARRAY`, `W3DNEW`, `WWASSERT`, `file_auto_ptr`, `StringClass`
