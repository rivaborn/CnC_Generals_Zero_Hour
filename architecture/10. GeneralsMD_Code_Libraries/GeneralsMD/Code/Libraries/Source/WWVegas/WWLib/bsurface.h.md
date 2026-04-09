# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bsurface.h

## Purpose
Defines a simple surface class that manages pixel data in system RAM.

## Responsibilities
- Encapsulates a 2D pixel buffer with width, height, and bytes-per-pixel.
- Provides locking mechanism for direct pixel access.
- Calculates stride and bytes-per-pixel for surface traversal.
- Inherits from XSurface for base surface functionality.

## Key Types
- BSurface (Class): A RAM-based surface wrapper with pixel buffer management.

## Key Functions
### BSurface/BSurface
- Purpose: Constructs a BSurface with given dimensions and optional buffer.
- Calls: XSurface constructor, Buffer constructor.

### BSurface/Lock
- Purpose: Returns a pointer to the pixel data at a given offset.
- Calls: XSurface::Lock().

### BSurface/Bytes_Per_Pixel
- Purpose: Returns the bytes per pixel value.
- Calls: None.

### BSurface/Stride
- Purpose: Returns the stride (width Ã bytes per pixel).
- Calls: Get_Width().

## Globals
- None.

## Dependencies
- `buff.h` (Buffer class)
- `xsurface.h` (XSurface base class)
- `Point2D` (for Lock offset)
