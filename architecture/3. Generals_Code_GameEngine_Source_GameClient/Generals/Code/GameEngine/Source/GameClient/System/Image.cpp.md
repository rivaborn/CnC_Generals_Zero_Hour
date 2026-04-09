# Generals/Code/GameEngine/Source/GameClient/System/Image.cpp

## Purpose
Manages high-level image representation for the game's GUI, handling image loading, parsing, and collection management.

## Responsibilities
- Parses image data from INI files
- Manages image collections and individual images
- Handles UV coordinate calculations and image status flags
- Loads mapped images from user data and game data directories

## Key Types
- **Image (Class)**: Represents a single image with texture data, UV coordinates, and status flags
- **ImageCollection (Class)**: Manages a collection of Image objects
- **ImageStatus (Enum)**: Defines image status flags (e.g., rotated, mirrored)

## Key Functions
### `parseImageCoords`
- Purpose: Parses image coordinate data from INI files and calculates UV coordinates
- Calls: `INI::scanInt`, `INI::getNextSubToken`

### `parseImageStatus`
- Purpose: Parses image status flags from INI files and adjusts image dimensions if rotated
- Calls: `INI::parseBitString32`, `BitTest`, `BitSet`, `BitClear`

### `ImageCollection::load`
- Purpose: Loads image data from INI files in specified directories
- Calls: `INI::loadDirectory`, `FindFirstFile`

## Globals
- **TheMappedImageCollection (ImageCollection*)**: Global pointer to the mapped image collection

## Dependencies
- Key includes: `PreRTS.h`, `BaseType.h`, `Debug.h`, `INI.h`, `GlobalData.h`, `Image.h`
- External symbols: `INI`, `TheGlobalData`, `BitTest`, `BitSet`, `BitClear`
