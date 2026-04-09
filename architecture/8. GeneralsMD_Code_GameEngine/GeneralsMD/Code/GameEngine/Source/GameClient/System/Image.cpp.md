# GeneralsMD/Code/GameEngine/Source/GameClient/System/Image.cpp

## Purpose
Manages high-level image representation for the game's GUI system, handling image loading, parsing, and UV coordinate management.

## Responsibilities
- Parses image data from INI files
- Manages image collections and lookups
- Handles UV coordinate calculations based on texture dimensions
- Supports image status flags (e.g., rotation)

## Key Types
- **Image (Class)**: Core image representation with texture, UV coords, and status
- **ImageCollection (Class)**: Manages a collection of images with name-based lookup
- **ImageStatus (Enum)**: Flags for image properties (rotation, etc.)

## Key Functions
### `parseImageCoords`
- Purpose: Parses image coordinates from INI and calculates UV coords
- Calls: `INI::scanInt`, `getNextSubToken`

### `parseImageStatus`
- Purpose: Parses image status flags and adjusts dimensions if rotated
- Calls: `INI::parseBitString32`, `BitTest`

### `ImageCollection::load`
- Purpose: Loads image definitions from INI files in specific directories
- Calls: `INI::loadDirectory`, `FindFirstFile`

## Globals
- **TheMappedImageCollection (ImageCollection*)**: Global pointer to the mapped images collection

## Dependencies
- `PreRTS.h`, `BaseType.h`, `INI.h`, `GlobalData.h`, `Image.h`, `NameKeyGenerator.h`
- Uses `std::map` for image storage
- Depends on `INI` class for parsing and `TheGlobalData` for paths
