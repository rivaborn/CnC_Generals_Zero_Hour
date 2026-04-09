# GeneralsMD/Code/GameEngine/Include/GameClient/Image.h

## Purpose
Defines high-level image representation classes for the game's GUI and rendering systems.

## Responsibilities
- Manages image metadata (UV coords, dimensions, texture data)
- Provides image collection and lookup functionality
- Supports INI-based image configuration parsing
- Handles image status flags (rotation, raw texture data)

## Key Types
- **Image (Class)**: Stores image properties (name, UV coords, dimensions, texture data)
- **ImageStatus (Enum)**: Flags for image state (rotation, raw texture data)
- **ImageCollection (Class)**: Manages a collection of images with lookup by name

## Key Functions
### Image::parseImageCoords
- Purpose: Parses image coordinate data from INI files
- Calls: Not inferable

### Image::parseImageStatus
- Purpose: Parses image status flags from INI files
- Calls: Not inferable

### ImageCollection::load
- Purpose: Loads images into the collection
- Calls: Not inferable

### ImageCollection::findImageByName
- Purpose: Finds an image by its name
- Calls: Not inferable

## Globals
- **TheMappedImageCollection (ImageCollection*)**: Global instance of the image collection

## Dependencies
- Common/AsciiString.h
- Common/GameMemory.h
- Common/SubsystemInterface.h
- <map>
- FieldParse, INI (forward declarations)
