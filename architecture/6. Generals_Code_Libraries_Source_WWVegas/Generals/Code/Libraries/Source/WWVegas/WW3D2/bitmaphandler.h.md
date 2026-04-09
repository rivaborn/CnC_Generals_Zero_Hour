# Generals/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.h

## Purpose
Provides utility functions for reading, writing, and converting pixel data between different color formats in the SAGE engine.

## Responsibilities
- Read pixel data from various formats into BGRA (D3D) format
- Write pixel data from BGRA format to various formats
- Copy pixels with optional color space conversion
- Generate mipmaps for textures
- Combine multiple BGRA pixels into one

## Key Types
- **BitmapHandlerClass (Class)**: Static utility class for bitmap operations
- **WW3DFormat (Enum)**: Not inferable (defined elsewhere)

## Key Functions
### BitmapHandlerClass::Read_B8G8R8A8
- Purpose: Read pixel data from various formats into BGRA format
- Calls: Bitmap_Assert

### BitmapHandlerClass::Write_B8G8R8A8
- Purpose: Write BGRA pixel data to various formats
- Calls: None

### BitmapHandlerClass::Copy_Pixel
- Purpose: Copy pixel with optional color space conversion
- Calls: Read_B8G8R8A8, Write_B8G8R8A8, Bitmap_Assert

### BitmapHandlerClass::Combine_A8R8G8B8
- Purpose: Combine four BGRA pixels into one
- Calls: None

### BitmapHandlerClass::Create_Mipmap_B8G8R8A8
- Purpose: Generate mipmap for a texture
- Calls: None

### BitmapHandlerClass::Copy_Image_Generate_Mipmap
- Purpose: Copy image and generate mipmaps
- Calls: Copy_Image, Create_Mipmap_B8G8R8A8

### BitmapHandlerClass::Copy_Image
- Purpose: Copy image data with optional color conversion and mipmap generation
- Calls: Copy_Pixel, Create_Mipmap_B8G8R8A8

## Globals
- None

## Dependencies
- Key includes: "always.h", "ww3dformat.h"
- External symbols: WW3DFormat, WWINLINE
