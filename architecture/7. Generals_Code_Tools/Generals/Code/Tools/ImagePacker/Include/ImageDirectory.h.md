# Generals/Code/Tools/ImagePacker/Include/ImageDirectory.h

## Purpose
Defines the `ImageDirectory` class for managing directories containing image files to be packed.

## Responsibilities
- Stores path to a directory containing images
- Tracks count of images in the directory
- Maintains linked list pointers for chaining directories

## Key Types
- **ImageDirectory (Class)**: Represents a directory containing images to be packed.

## Key Functions
### ImageDirectory::ImageDirectory
- Purpose: Default constructor initializing members to NULL/0.
- Calls: None.

### ImageDirectory::~ImageDirectory
- Purpose: Destructor that deletes the path string.
- Calls: `delete m_path`.

## Globals
- None.

## Dependencies
- Uses `UnsignedInt` (likely from a system header).
- No external symbols defined here.
