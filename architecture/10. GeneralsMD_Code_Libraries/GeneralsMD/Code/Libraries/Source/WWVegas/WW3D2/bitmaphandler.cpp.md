# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.cpp

## Purpose
Handles bitmap operations including copying, mipmap generation, and color space conversion for the WW3D2 rendering system.

## Responsibilities
- Bitmap copying with format conversion
- Mipmap generation for textures
- Color space transformations (HSV shifts)
- Bumpmap generation from color data

## Key Types
- `BitmapHandlerClass` (Class): Manages bitmap operations
- `WW3DFormat` (Enum): Pixel format identifiers

## Key Functions
### `Bitmap_Assert`
- Purpose: Wrapper for assertion checks
- Calls: `WWASSERT`

### `Create_Mipmap_B8G8R8A8`
- Purpose: Generates a mipmap level from a 32-bit source
- Calls: `Combine_A8R8G8B8`

### `Copy_Image_Generate_Mipmap`
- Purpose: Copies an image while generating a mipmap level
- Calls: `Combine_A8R8G8B8`, `Recolor`, `Read_B8G8R8A8`, `Write_B8G8R8A8`

### `Copy_Image`
- Purpose: Copies an image with optional scaling, format conversion, and mipmap generation
- Calls: `Get_Bytes_Per_Pixel`, `Read_B8G8R8A8`, `Write_B8G8R8A8`, `Recolor`, `Copy_Pixel`

## Globals
- None

## Dependencies
- `bitmaphandler.h`
- `wwdebug.h`
- `colorspace.h`
- `Vector3` (external)
- `WWASSERT` (macro)
- `Combine_A8R8G8B8` (external)
- `Recolor` (external)
- `Read_B8G8R8A8` (external)
- `Write_B8G8R8A8` (external)
- `Copy_Pixel` (external)
- `Get_Bytes_Per_Pixel` (external)
