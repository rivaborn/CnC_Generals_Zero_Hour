# Generals/Code/Tools/ImagePacker/Source/ImageInfo.cpp

## Purpose
Manages image metadata for texture packing in the ImagePacker tool.

## Responsibilities
- Initializes and cleans up image information
- Tracks image dimensions, paths, and packing status
- Manages links to texture pages and neighboring images
- Handles memory for string fields (path, filenames)

## Key Types
- `ImageInfo` (Class): Stores metadata for an image to be packed into texture pages

## Key Functions
### `ImageInfo::ImageInfo()`
- Purpose: Default constructor initializing all member variables
- Calls: None

### `ImageInfo::~ImageInfo()`
- Purpose: Destructor that cleans up dynamically allocated string members
- Calls: `delete []` for `m_path`, `m_filenameOnly`, `m_filenameOnlyNoExt`

## Globals
- None

## Dependencies
- Key includes: `<stdlib.h>`, `"ImageInfo.h"`
- External symbols: `NULL` (from `<stdlib.h>`)
