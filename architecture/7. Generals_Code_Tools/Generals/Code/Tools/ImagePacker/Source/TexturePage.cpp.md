# Generals/Code/Tools/ImagePacker/Source/TexturePage.cpp

## Purpose
Manages texture pages for image packing, including fitting images into pages, extending image edges, and generating final texture data.

## Responsibilities
- Pack images into texture pages with gutters and borders
- Extend image edges to fill borders
- Generate final packed texture data
- Write texture data to TGA files
- Provide pixel access for debugging

## Key Types
- **TexturePage (Class)**: Represents a texture page containing packed images
- **ImageInfo (Struct)**: Holds image metadata (size, position, status flags)
- **Targa (Class)**: External TGA file handler

## Key Functions
### `extendToRowIfOpen`
- Purpose: Extends pixel data to adjacent rows if they are "open" (transparent/black)
- Calls: None

### `extendImageEdges`
- Purpose: Bleeds image edges outward into borders
- Calls: `extendToRowIfOpen`

### `addImage`
- Purpose: Finds optimal position for an image on the texture page
- Calls: `buildFitRegion`, `spotUsed`, `lineUsed`, `markRegionUsed`

### `generateTexture`
- Purpose: Generates final packed texture from all images
- Calls: `addImageData`

### `writeFile`
- Purpose: Writes texture data to a TGA file
- Calls: `Targa::Save`

### `getPixel`
- Purpose: Retrieves RGB/A pixel data at specified coordinates
- Calls: None

## Globals
- **TheImagePacker (External)**: Global ImagePacker instance

## Dependencies
- `Common/Debug.h` (for assertions)
- `TexturePage.h` (class definition)
- `ImagePacker.h` (global access)
- `Targa` class (external TGA handler)
- `BitTest`, `BitSet`, `BitClear` (bit manipulation macros)
