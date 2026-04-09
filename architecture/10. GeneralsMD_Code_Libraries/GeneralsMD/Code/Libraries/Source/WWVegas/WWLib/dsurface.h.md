# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/dsurface.h

## Purpose
Defines the `DSurface` class, a DirectDraw-based surface implementation for rendering operations in the game engine.

## Responsibilities
- Manages DirectDraw surfaces (creation, locking, blitting, filling)
- Handles device context operations for GDI compatibility
- Provides pixel format and memory layout queries
- Supports primary surface creation and management

## Key Types
- **DSurface (Class)**: DirectDraw-based surface implementation
- **BASECLASS (Class)**: Base class (XSurface)

## Key Functions
### DSurface::Create_Primary
- Purpose: Creates a primary surface (visible screen)
- Calls: Not inferable

### DSurface::Blit_From
- Purpose: Copies regions between surfaces with optional transparency
- Calls: XSurface::Blit_From

### DSurface::Lock/Unlock
- Purpose: Locks/unlocks surface memory for direct access
- Calls: Not inferable

### DSurface::Fill_Rect
- Purpose: Fills a rectangular region with a color
- Calls: Not inferable

### DSurface::GetDC/ReleaseDC
- Purpose: Gets/releases a Windows device context for GDI operations
- Calls: Not inferable

## Globals
- **Clipper (LPDIRECTDRAWCLIPPER)**: Static clipper for primary surface
- **PixelFormat (DDPIXELFORMAT)**: Primary surface pixel format
- **RedRight/RedLeft/BlueRight/BlueLeft/GreenRight/GreenLeft (int)**: Shift values for color extraction
- **ThisRedRight/ThisRedLeft/ThisBlueRight/ThisBlueLeft/ThisGreenRight/ThisGreenLeft (int)**: Surface-specific shift values
- **HalfbrightMask/QuarterbrightMask/EighthbrightMask (unsigned short)**: Precomputed brightness masks

## Dependencies
- `palette.h`, `win.h`, `xsurface.h`, `ddraw.h`
- DirectDraw API (LPDIRECTDRAWSURFACE, DDSURFACEDESC)
- XSurface base class methods
