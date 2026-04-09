# Generals/Code/Tools/ImagePacker/Include/ImageInfo.h

## Purpose
Defines the `ImageInfo` class for managing image metadata during texture packing in the ImagePacker tool.

## Responsibilities
- Stores image file paths, dimensions, and processing status
- Tracks texture page placement and fitting parameters
- Manages linked list of images per texture page
- Defines status and fitting flags as enums

## Key Types
- **ImageInfo (Class)**: Container for image metadata and packing state
- **TexturePage (Class)**: Forward-declared reference to texture page class
- **Anonymous Enum (Enum)**: Image processing status flags (UNPACKED, PACKED, etc.)
- **Anonymous Enum (Enum)**: Image fitting region flags (FIT_XGUTTER, etc.)

## Key Functions
### ImageInfo()
- Purpose: Default constructor for ImageInfo
- Calls: None

### ~ImageInfo()
- Purpose: Destructor for ImageInfo
- Calls: None

## Globals
- None

## Dependencies
- `Lib/BaseType.h` (for Int, UnsignedInt, ICoord2D, IRegion2D)
- `TexturePage` class (forward-declared)
