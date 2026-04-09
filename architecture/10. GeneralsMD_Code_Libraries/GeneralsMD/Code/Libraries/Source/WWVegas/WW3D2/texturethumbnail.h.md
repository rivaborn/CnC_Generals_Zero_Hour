# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texturethumbnail.h

## Purpose
Header file defining classes for managing and creating texture thumbnails in the game engine.

## Responsibilities
- Define `ThumbnailClass` for storing thumbnail data
- Define `ThumbnailManagerClass` for managing thumbnails
- Provide interface for thumbnail creation, loading, and saving
- Handle thumbnail caching and memory management

## Key Types
- **ThumbnailClass (Class)**: Represents a texture thumbnail with metadata
- **ThumbnailManagerClass (Class)**: Manages a collection of thumbnails and their persistence
- **WW3DFormat (Enum)**: Texture format type (external)

## Key Functions
### ThumbnailClass constructor (private)
- Purpose: Creates a thumbnail instance with specified parameters
- Calls: None visible

### ThumbnailManagerClass::Create_Thumbnails
- Purpose: Generates thumbnails for textures
- Calls: Not inferable

### ThumbnailManagerClass::Load/Save
- Purpose: Persists thumbnails to/from disk
- Calls: Not inferable

### ThumbnailManagerClass::Peek_Thumbnail_Instance
- Purpose: Retrieves a thumbnail by name
- Calls: Not inferable

## Globals
- **CreateThumbnailIfNotFound (bool)**: Static flag controlling automatic thumbnail generation
- **ThumbnailFileName (StringClass)**: Filename for thumbnail storage
- **MixFileName (StringClass)**: Associated mix file name

## Dependencies
- `wwstring.h`, `hashtemplate.h`, `dllist.h`, `ww3dformat.h`
- `StringClass`, `HashTemplateClass`, `DLNodeClass`
