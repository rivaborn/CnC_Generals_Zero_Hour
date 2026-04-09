# Generals/Code/Libraries/Source/WWVegas/WW3D2/surfaceclass.cpp

## Purpose
Implements the SurfaceClass for handling Direct3D surfaces, including pixel manipulation, format conversion, and surface operations.

## Responsibilities
- Manages Direct3D surface creation, locking/unlocking, and memory operations
- Provides pixel-level manipulation (get/set, drawing primitives)
- Handles pixel format conversions and color space operations
- Implements surface analysis (transparency, monochrome detection)
- Supports hue shifting and recoloring

## Key Types
- SurfaceClass: Wrapper for Direct3D surfaces with utility functions
- SurfaceDescription (struct): Describes surface format, width, and height
- WW3DFormat (enum): Pixel format identifiers (e.g., WW3D_FORMAT_A8R8G8B8)

## Key Functions
### PixelSize
- Purpose: Returns byte size of a pixel for a given surface format
- Calls: None

### Convert_Pixel (Vector3 overload)
- Purpose: Converts pixel data to RGB vector
- Calls: None

### Convert_Pixel (unsigned char overload)
- Purpose: Converts RGB vector to pixel data
- Calls: None

### SurfaceClass::Clear
- Purpose: Clears surface to zero
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::Copy (byte array)
- Purpose: Copies data from byte array to surface
- Calls: PixelSize, Lock, Unlock

### SurfaceClass::DrawPixel
- Purpose: Draws a single pixel at specified coordinates
- Calls: Lock, Unlock

### SurfaceClass::DrawHLine
- Purpose: Draws a horizontal line
- Calls: Lock, Unlock

### SurfaceClass::Hue_Shift
- Purpose: Applies hue shift to surface pixels
- Calls: Lock, Unlock, Convert_Pixel, Recolor, Bound

### SurfaceClass::Is_Monochrome
- Purpose: Checks if surface contains only grayscale pixels
- Calls: Lock, Unlock, Convert_Pixel

### SurfaceClass::Is_Transparent_Column
- Purpose: Tests if a column contains transparent pixels
- Calls: Lock, Unlock

## Globals
None

## Dependencies
- surfaceclass.h (header)
- formconv.h (format conversion)
- dx8wrapper.h (Direct3D wrapper)
- vector2i.h (2D vector)
- colorspace.h (color operations)
- bound.h (clamping)
- <d3dx8.h> (Direct3D headers)
