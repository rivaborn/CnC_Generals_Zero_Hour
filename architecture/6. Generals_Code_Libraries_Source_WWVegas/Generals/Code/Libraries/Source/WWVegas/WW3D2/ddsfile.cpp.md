# Generals/Code/Libraries/Source/WWVegas/WW3D2/ddsfile.cpp

## Purpose
Handles loading, parsing, and rendering of DDS (DirectDraw Surface) texture files, supporting DXT1-5 compression formats.

## Responsibilities
- Loads DDS files and parses headers
- Manages mipmap levels and texture reduction
- Converts DXT-compressed textures to various formats
- Provides pixel access and block decompression

## Key Types
- **DDSFileClass**: Main class for DDS file handling
- **LegacyDDSURFACEDESC2**: DDS header structure (external)
- **WW3DFormat**: Texture format enum (external)

## Key Functions
### `RGB565_To_ARGB8888`
- Purpose: Converts 16-bit RGB565 color to 32-bit ARGB8888
- Calls: None

### `Combine_Colors`
- Purpose: Interpolates between two colors based on a relative value
- Calls: None

### `Get_Pixel`
- Purpose: Extracts a single pixel from a compressed texture block
- Calls: `RGB565_To_ARGB8888`, `Combine_Colors`

### `Get_4x4_Block`
- Purpose: Decompresses a 4x4 block from DXT-compressed texture
- Calls: `RGB565_To_ARGB8888`, `Combine_Colors`, `BitmapHandlerClass::Write_B8G8R8A8`

## Globals
- None

## Dependencies
- `ddsfile.h`, `ffactory.h`, `bufffile.h`, `formconv.h`, `dx8wrapper.h`, `bitmaphandler.h`
- `D3DFORMAT`, `IDirect3DSurface8` (DirectX 8)
- `WW3DFormat`, `LegacyDDSURFACEDESC2` (external types)
