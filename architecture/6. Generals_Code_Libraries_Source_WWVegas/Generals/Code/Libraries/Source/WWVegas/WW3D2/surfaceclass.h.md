# Generals/Code/Libraries/Source/WWVegas/WW3D2/surfaceclass.h

## Purpose
Defines the `SurfaceClass` wrapper for Direct3D surfaces, providing surface manipulation and rendering capabilities.

## Responsibilities
- Wraps `IDirect3DSurface8` for surface operations
- Provides pixel manipulation, copying, and rendering functions
- Manages surface memory and format
- Supports font rendering operations

## Key Types
- `SurfaceClass` (Class): Wrapper for Direct3D surfaces with manipulation methods
- `SurfaceDescription` (Struct): Holds surface format, width, and height
- `IDirect3DSurface8` (Class): Direct3D surface interface (external)
- `Vector2i` (Class): 2D integer vector (external)
- `Vector3` (Class): 3D vector (external)

## Key Functions
### `SurfaceClass(unsigned width, unsigned height, WW3DFormat format)`
- Purpose: Creates a surface with specified dimensions and format
- Calls: Not inferable

### `Copy(unsigned int dstx, unsigned int dsty, unsigned int srcx, unsigned int srcy, unsigned int width, unsigned int height, const SurfaceClass *other)`
- Purpose: Copies a rectangular region from one surface to another
- Calls: Not inferable

### `Stretch_Copy(unsigned int dstx, unsigned int dsty, unsigned int dstwidth, unsigned int dstheight, unsigned int srcx, unsigned int srcy, unsigned int srcwidth, unsigned int srcheight, const SurfaceClass *source)`
- Purpose: Stretches and copies a surface region
- Calls: Not inferable

### `DrawHLine(const unsigned int y, const unsigned int x1, const unsigned int x2, unsigned int color)`
- Purpose: Draws a horizontal line on the surface
- Calls
