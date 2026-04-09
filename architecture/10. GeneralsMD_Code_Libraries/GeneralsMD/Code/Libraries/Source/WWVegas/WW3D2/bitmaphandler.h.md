# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.h

## Purpose
Provides utility functions for reading, writing, and converting pixel data between different color formats in the SAGE engine.

## Responsibilities
- Pixel format conversion (read/write)
- Color space manipulation (HSV shifts)
- Mipmap generation
- Palette-based color lookup

## Key Types
- **BitmapHandlerClass (Class)**: Static utility class for bitmap operations.
- **WW3DFormat (Enum)**: Not inferable (external type).
- **Vector3 (Struct)**: Not inferable (external type).

## Key Functions
### `Read_B8G8R8A8`
- Purpose: Reads a pixel in B8G8R8A8 format from various source formats.
- Calls: `Bitmap_Assert`, `Get_Bytes_Per_Pixel`.

### `Write_B8G8R8A8`
- Purpose: Writes a pixel in B8G8R8A8 format to various destination formats.
- Calls: `Bitmap_Assert`.

### `Copy_Pixel`
- Purpose: Copies a pixel between formats with optional HSV recoloring.
- Calls: `Read_B8G8R8A8`, `Write_B8G8R8A8`, `Recolor`.

### `Combine_A8R8G8B8`
- Purpose: Combines four BGRA pixels into one with alpha blending.
- Calls: None.

### `Create_Mipmap_B8G8R8A8`
- Purpose: Generates a mipmap level from a source surface.
- Calls: None.

### `Copy_Image_Generate_Mipmap`
- Purpose: Copies an image and generates mipmaps.
- Calls: `Copy_Pixel`, `Create_Mipmap_B8G8R8A8`.

### `Copy_Image`
- Purpose: Copies an image with optional mipmap generation and HSV shift.
- Calls: `Copy_Image_Generate_Mipmap`.

## Globals
- None.

## Dependencies
- `always.h`, `ww3dformat.h`, `vector3.h`, `colorspace.h`
- `Bitmap_Assert`, `Get_Bytes_Per_Pixel`, `Recolor` (external functions).
