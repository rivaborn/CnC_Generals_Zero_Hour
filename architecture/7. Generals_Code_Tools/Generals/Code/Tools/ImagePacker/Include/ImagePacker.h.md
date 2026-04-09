# Generals/Code/Tools/ImagePacker/Include/ImagePacker.h

## Purpose
Header for the ImagePacker class, a tool for packing multiple images into texture atlases.

## Responsibilities
- Manage image packing into texture pages
- Handle user settings (gutter size, gap methods, alpha output)
- Generate INI files for packed textures
- Provide preview functionality via Windows HWND

## Key Types
- **ImagePacker (Class)**: Main class for image packing operations.
- **(anonymous enum)**: Defines gap methods (EXTEND_RGB, GUTTER).
- **GAP_METHOD_EXTEND_RGB (Enum)**: Extend RGB (no alpha) of image on all sides.
- **GAP_METHOD_GUTTER (Enum)**: Put transparent gutter on right and bottom side of image.

## Key Functions
### `ImagePacker::process`
- Purpose: Run the image packing process.
- Calls: `validateImages`, `packImages`, `writeFinalTextures`, `generateINIFile`.

### `ImagePacker::packImages`
- Purpose: Perform the actual packing of images into texture pages.
- Calls: `createNewTexturePage`, `sortImageList`.

### `ImagePacker::generateINIFile`
- Purpose: Generate an INI file for the packed texture set.
- Calls: Not inferable (implementation in .cpp).

## Globals
- **TheImagePacker (ImagePacker*)**: Global instance of the ImagePacker class.

## Dependencies
- **Includes**: `windows.h`, `BaseType.h`, `Targa.h`, `ImageDirectory.h`, `ImageInfo.h`, `TexturePage.h`
- **External Types**: `ICoord2D`, `Targa`, `ImageDirectory`, `ImageInfo`, `TexturePage`
- **External Functions**: `BitSet`, `BitClear` (bit manipulation utilities)
