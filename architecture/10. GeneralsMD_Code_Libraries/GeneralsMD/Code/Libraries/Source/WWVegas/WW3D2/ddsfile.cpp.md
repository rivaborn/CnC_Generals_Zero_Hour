# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ddsfile.cpp

## Purpose
Handles DirectDraw Surface (DDS) texture file loading, mipmapping, and pixel data extraction for the SAGE engine.

## Responsibilities
- Loads DDS files with DXT1-5 compression
- Manages mipmap levels and texture dimensions
- Converts between color formats (RGB565 â ARGB8888)
- Extracts pixel/block data from compressed textures
- Supports cube maps and volume textures

## Key Types
- `DDSFileClass` (Class): Main DDS file handler
- `WW3DFormat` (Enum): Texture format identifiers (DXT1-5)
- `DDSType` (Enum): Texture type (normal/cube/volume)

## Key Functions
### `RGB565_To_ARGB8888`
- Purpose: Converts 16-bit RGB565 to 32-bit ARGB8888
- Calls: None

### `ARGB8888_To_RGB565`
- Purpose: Converts 32-bit ARGB8888 to 16-bit RGB565
- Calls: None

### `Combine_Colors`
- Purpose: Blends two colors with specified ratio
- Calls: None

### `Get_Pixel`
- Purpose: Extracts pixel color from compressed texture at given coordinates
- Calls: `RGB565_To_ARGB8888`, `Combine_Colors`

### `Get_4x4_Block`
- Purpose: Decompresses a 4x4 block from DXT-compressed texture
- Calls: `RGB565_To_ARGB8888`, `Combine_Colors`, `Recolor`

## Globals
- None

## Dependencies
- `ddsfile.h`, `ffactory.h`, `bufffile.h`, `formconv.h`, `dx8wrapper.h`, `bitmaphandler.h`, `colorspace.h`
- DirectX 8 headers (`ddraw.h`)
- `W3DNEWARRAY`, `MSGW3DNEWARRAY` memory allocation macros
