# Generals/Code/Libraries/Source/WWVegas/WW3D2/texturethumbnail.h

## Purpose
Defines the `ThumbnailClass` for managing texture thumbnails in the game engine.

## Responsibilities
- Encapsulates texture thumbnail data (name, bitmap, dimensions)
- Provides accessors for thumbnail properties
- Manages singleton instance via static methods
- Handles initialization/deinitialization of thumbnail system

## Key Types
- **ThumbnailClass (Class)**: Manages texture thumbnail data and access.

## Key Functions
### ThumbnailClass/ThumbnailClass (const char* name, unsigned char* bitmap, unsigned w, unsigned h, bool allocated)
- Purpose: Constructs a thumbnail from raw bitmap data.
- Calls: None

### ThumbnailClass/ThumbnailClass (const StringClass& filename)
- Purpose: Constructs a thumbnail by loading from a file.
- Calls: None

### ThumbnailClass/~ThumbnailClass
- Purpose: Destroys the thumbnail and frees allocated memory if needed.
- Calls: None

### ThumbnailClass/Peek_Bitmap
- Purpose: Returns the raw bitmap data.
- Calls: None

### ThumbnailClass/Get_Width
- Purpose: Returns the thumbnail width.
- Calls: None

### ThumbnailClass/Get_Height
- Purpose: Returns the thumbnail height.
- Calls: None

### ThumbnailClass/Get_Name
- Purpose: Returns the thumbnail name.
- Calls: None

### ThumbnailClass/Peek_Instance
- Purpose: Retrieves a thumbnail instance by name.
- Calls: None

### ThumbnailClass/Init
- Purpose: Initializes the thumbnail system.
- Calls: None

### ThumbnailClass/Deinit
- Purpose: Deinitializes the thumbnail system.
- Calls: None

## Globals
- None

## Dependencies
- `always.h`
