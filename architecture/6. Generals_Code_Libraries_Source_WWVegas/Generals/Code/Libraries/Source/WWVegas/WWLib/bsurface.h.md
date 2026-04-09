# Generals/Code/Libraries/Source/WWVegas/WWLib/bsurface.h

## Purpose
Defines a system RAM-based surface class for pixel data manipulation.

## Responsibilities
- Manages a buffer-backed surface with configurable bytes-per-pixel
- Provides pixel access via locking mechanism
- Calculates stride and bytes-per-pixel for surface operations
- Inherits from XSurface for base functionality

## Key Types
- BSurface (Class): System RAM surface wrapper with buffer management

## Key Functions
### BSurface/BSurface
- Purpose: Constructs a surface with given dimensions and bytes-per-pixel
- Calls: XSurface constructor, Buffer constructor

### BSurface/Lock
- Purpose: Returns a pointer to the surface buffer at a given offset
- Calls: XSurface::Lock()

### BSurface/Bytes_Per_Pixel
- Purpose: Returns the bytes per pixel value
- Calls: None

### BSurface/Stride
- Purpose: Returns the surface stride (width * bytes per pixel)
- Calls: Get_Width()

## Globals
- None

## Dependencies
- buff.h (Buffer class)
- xsurface.h (XSurface base class)
- Point2D (used in Lock parameter)
