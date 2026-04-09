# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/surfaceclass.cpp

## Purpose
Implements the SurfaceClass for handling Direct3D surfaces, including pixel manipulation, format conversion, and surface operations.

## Responsibilities
- Manages Direct3D surface creation, locking, and memory operations
- Provides pixel-level manipulation (get/set/draw)
- Handles pixel format conversions and color space operations
- Supports surface copying and region operations
- Implements surface analysis (transparency, monochrome detection)

## Key Types
- SurfaceClass: Wrapper for Direct3D surfaces with utility functions
- SurfaceDescription (struct): Describes surface format, width, and height
- WW3DFormat (enum): Defines supported pixel formats

## Key Functions
### PixelSize
- Purpose: Returns byte size of a pixel for a given format
- Calls: None

### Convert_Pixel (Vector3 â pixel)
- Purpose: Converts RGB vector to pixel data for a specific format
- Calls: None

### Convert_Pixel (pixel â Vector3)
- Purpose: Converts pixel data to RGB vector for a specific format
- Calls: None

### SurfaceClass::Clear
- Purpose: Clears surface to zero values
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::Copy (byte array)
- Purpose: Copies data from byte array to surface
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::Is_Transparent_Column
- Purpose: Checks if a column contains any non-transparent pixels
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::Get_Pixel
- Purpose: Retrieves RGB values at a specific coordinate
- Calls: Convert_Pixel, Lock, Unlock

### SurfaceClass::DrawPixel
- Purpose: Draws a single pixel at specified coordinates
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::DrawHLine
- Purpose: Draws a horizontal line segment
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::Is_Monochrome
- Purpose: Determines if surface contains only grayscale pixels
- Calls: PixelSize, Lock, Unlock, Convert_Pixel

### SurfaceClass::Hue_Shift
- Purpose: Applies hue/saturation/value shift to surface pixels
- Calls: PixelSize, Lock, Unlock, Convert_Pixel, Recolor, Bound

## Globals
None

## Dependencies
- surfaceclass.h (header)
- formconv.h (format conversion)
- dx8wrapper.h (Direct3D wrapper)
- vector2i.h (2D vector)
- colorspace.h (color operations)
- bound.h (value clamping)
- <d3dx8.h> (Direct3D headers)
- Direct3D 8 interfaces (IDirect3DSurface8)
