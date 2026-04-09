# Generals/Code/Tools/ImagePacker/Source/ImagePacker.cpp

## Purpose
Handles packing multiple image files into optimized texture atlases for the game engine.

## Responsibilities
- Loads and validates images from directories
- Packs images into texture pages using space optimization
- Generates output TGA files and INI definitions
- Provides UI for configuration and progress feedback

## Key Types
- **ImagePacker (Class)**: Main controller for the image packing process
- **TexturePage (Class)**: Represents a single packed texture page
- **ImageInfo (Class)**: Contains metadata about individual images
- **ImageDirectory (Class)**: Tracks directories containing source images

## Key Functions
### `sortImageCompare`
- Purpose: Comparison function for sorting images by area (descending)
- Calls: None

### `validateImages`
- Purpose: Checks images for processing compatibility (size/format)
- Calls: `BitSet`, `DEBUG_ASSERTCRASH`, `DialogBox`

### `packImages`
- Purpose: Main packing algorithm that places images onto texture pages
- Calls: `validateImages`, `createNewTexturePage`, `TexturePage::addImage`

### `writeFinalTextures`
- Purpose: Generates and writes packed texture files
- Calls: `TexturePage::generateTexture`, `TexturePage::writeFile`, `DialogBox`

### `generateINIFile`
- Purpose: Creates INI file mapping original images to texture coordinates
- Calls: `fopen`, `fprintf`, `fclose`

## Globals
- **gAppPrefix (char*)**: Prefix for debug log files ("ip_")
- **TheImagePacker (ImagePacker*)**: Singleton instance of the packer

## Dependencies
- `Common/Debug.h`, `WWLib/Targa.h`, `Resource.h`, `ImagePacker.h`, `WinMain.h`, `WindowProc.h`
- Windows API (`FindFirstFile`, `DialogBox`, etc.)
- Standard C (`qsort`, `fopen`, etc.)
