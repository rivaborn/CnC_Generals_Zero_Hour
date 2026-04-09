# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/dsurface.cpp

## Purpose
Implements DirectDraw surface management for the SAGE engine, handling surface creation, blitting, locking, and pixel format operations.

## Responsibilities
- Manages DirectDraw surfaces (primary and offscreen)
- Provides blitting and filling operations with clipping
- Handles surface locking/unlocking and memory restoration
- Supports high-color pixel format operations
- Manages surface pixel format and stride information

## Key Types
- DSurface (Class): DirectDraw surface wrapper with blitting and locking capabilities
- DDPIXELFORMAT (Struct): Pixel format description for DirectDraw surfaces

## Key Functions
### DSurface::DSurface(int width, int height, bool system_memory, DDPIXELFORMAT *pixform)
- Purpose: Creates an offscreen DirectDraw surface
- Calls: DirectDrawObject->CreateSurface, SurfacePtr->GetSurfaceDesc

### DSurface::Create_Primary(DSurface ** backsurface1)
- Purpose: Creates the primary (visible) surface with optional backbuffer
- Calls: DirectDrawObject->CreateSurface, SurfacePtr->GetSurfaceDesc

### DSurface::Lock(Point2D point) const
- Purpose: Locks surface memory and returns pointer to specified pixel
- Calls: Restore_Check, SurfacePtr->Lock, XSurface::Lock

### DSurface::Blit_From(Rect const & dcliprect, Rect const & destrect, Surface const & ssource, Rect const & scliprect, Rect const & sourcerect, bool trans)
- Purpose: Blits from one surface to another with clipping
- Calls: Restore_Check, XSurface::Blit_From, SurfacePtr->Blt

### DSurface::Fill_Rect(Rect const & cliprect, Rect const & fillrect, int color)
- Purpose: Fills a rectangle with specified color using clipping
- Calls: Restore_Check, XSurface::Fill_Rect, SurfacePtr->Blt

## Globals
- DirectDrawObject (LPDIRECTDRAW): Pointer to DirectDraw object
- PaletteSurface (LPDIRECTDRAWSURFACE): Pointer to palette surface
- Clipper (LPDIRECTDRAWCLIPPER): Clipper object for primary surface
- RedRight/RedLeft/BlueRight/BlueLeft/GreenRight/GreenLeft (int): Pixel format shift values
- HalfbrightMask/QuarterbrightMask/EighthbrightMask (unsigned short): Brightness masks
- PixelFormat (DDPIXELFORMAT): Current pixel format

## Dependencies
- dsurface.h (header)
- always.h (engine includes)
- <assert.h> (standard library)
- DirectDraw API (IDirectDraw, IDirectDrawSurface, etc.)
- XSurface base class methods
