# Generals/Code/Tools/ImagePacker/Include/TexturePage.h

## Purpose
Defines the `TexturePage` class for packing multiple images into a single texture atlas.

## Responsibilities
- Manages a texture canvas and packed image data
- Handles image placement and border extension
- Generates and saves final packed texture files
- Tracks usage status and error conditions

## Key Types
- **TexturePage (Class)**: Represents a texture page containing packed images
- **FREE (Enum)**: Open pixel state
- **USED (Enum)**: Used pixel state
- **READY (Enum)**: Texture page status flags
- **PAGE_ERROR (Enum)**: Error status flags
- **CANT_ALLOCATE_PACKED_IMAGE (Enum)**: Allocation error flag
- **CANT_ADD_IMAGE_DATA (Enum)**: Data addition error flag
- **NO_TEXTURE_DATA (Enum)**: Missing texture data flag
- **ERROR_DURING_SAVE (Enum)**: Save error flag

## Key Functions
### TexturePage::addImage
- Purpose: Attempts to add an image to the texture page
- Calls: Not inferable

### TexturePage::generateTexture
- Purpose: Generates the final packed texture
- Calls: Not inferable

### TexturePage::writeFile
- Purpose: Writes the generated texture to a file
- Calls: Not inferable

### TexturePage::buildFitRegion
- Purpose: Builds a region to fit an image with given constraints
- Calls: Not inferable

### TexturePage::addImageData
- Purpose: Adds actual image data to the destination buffer
- Calls: Not inferable

### TexturePage::extendImageEdges
- Purpose: Extends image edges outward into border if present
- Calls: Not inferable

## Globals
- None

## Dependencies
- `WWLib/Targa.h`
- `
