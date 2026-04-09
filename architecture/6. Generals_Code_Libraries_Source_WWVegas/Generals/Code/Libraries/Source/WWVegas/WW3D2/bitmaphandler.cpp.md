# Generals/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.cpp

## Purpose
Handles bitmap operations including copying, scaling, format conversion, and mipmap generation for the W3D rendering engine.

## Responsibilities
- Bitmap format conversion and pixel manipulation
- Mipmap generation for textures
- Bumpmap calculation from source images
- Surface copying with scaling and color space conversion

## Key Types
- `BitmapHandlerClass`: Main class for bitmap operations
- `WW3DFormat` (Enum): Pixel format identifiers (e.g., `WW3D_FORMAT_A8R8G8B8`)

## Key Functions
### `Bitmap_Assert(bool condition)`
- Purpose: Wrapper for assertion checking
- Calls: `WWASSERT`

### `BitmapHandlerClass::Create_Mipmap_B8G8R8A8()`
- Purpose: Generates a mipmap level from a 32-bit source
- Calls: `Combine_A8R8G8B8`

### `BitmapHandlerClass::Copy_Image_Generate_Mipmap()`
- Purpose: Copies an image while generating a mipmap level
- Calls: `Combine_A8R8G8B8`, `Read_B8G8R8A8`, `Write_B8G8R8A8`, `Get_Bytes_Per_Pixel`

### `BitmapHandlerClass::Copy_Image()`
- Purpose: Copies and scales images with format conversion and optional mipmap generation
- Calls: `WWASSERT`, `Read_B8G8R8A8`, `Write_B8G8R8A8`, `Get_Bytes_Per_Pixel`, `Copy_Pixel`, `Combine_A8R8G8B8`

## Globals
None

## Dependencies
- `bitmaphandler.h` (header)
- `wwdebug.h` (for `WWASSERT`)
- External functions: `Combine_A8R8G8B8`, `Read_B8G8R8A8`, `Write_B8G8R8A8`, `Get_Bytes_Per_Pixel`, `Copy_Pixel`
