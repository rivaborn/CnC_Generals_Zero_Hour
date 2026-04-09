# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texturethumbnail.cpp

## Purpose
Manages texture thumbnails for the game, handling loading, caching, and updating of thumbnail images from TGA/DDS files.

## Responsibilities
- Load and cache texture thumbnails from mix files
- Manage thumbnail creation and updates
- Handle thumbnail storage and retrieval via hash tables
- Support global and per-manager thumbnail databases
- Validate thumbnail freshness against source textures

## Key Types
- **ThumbnailClass**: Represents a single texture thumbnail with bitmap data and metadata
- **ThumbnailManagerClass**: Manages a collection of thumbnails and their persistence
- **HashTemplateClass<StringClass, ThumbnailClass\*>**: Hash table for thumbnail lookup

## Key Functions
### Create_Hash_Name
- Purpose: Generates a hash-friendly name from a thumbnail filename
- Calls: None

### ThumbnailClass::ThumbnailClass (filename constructor)
- Purpose: Loads a texture thumbnail from TGA or DDS file
- Calls: DDSFileClass::Load, Targa::Open, BitmapHandlerClass::Copy_Image

### ThumbnailManagerClass::Create_Thumbnails
- Purpose: Scans mix files and creates thumbnails for all textures
- Calls: MixFileFactoryClass methods, ThumbnailClass constructor

### ThumbnailManagerClass::Update_Thumbnail_File
- Purpose: Updates thumbnail database when mix files change
- Calls: FileClass operations, ThumbnailManagerClass::Create_Thumbnails

### ThumbnailManagerClass::Pre_Init
- Purpose: Initializes all thumbnail databases before game start
- Calls: Update_Thumbnail_File, Windows API file operations

## Globals
- **ThumbnailManagerList** (DLListClass<ThumbnailManagerClass>): List of active thumbnail managers
- **GlobalThumbnailManager** (ThumbnailManagerClass*): Singleton global thumbnail manager
- **message_box_displayed** (bool): Tracks if update message was shown
- **ThumbFileHeader** (const char*): Magic number for thumbnail files

## Dependencies
- Key includes: texturethumbnail.h, hashtemplate.h, targa.h, ddsfile.h, textureloader.h
- External symbols: W3DNEWARRAY, WWPROFILE, WWASSERT, _TheFileFactory
- Windows API: MessageBox, FindFirstFile, GetCurrentDirectory
