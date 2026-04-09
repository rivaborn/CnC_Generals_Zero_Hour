# Generals/Code/Libraries/Source/WWVegas/WWLib/dsurface.h

## Purpose
Declares the `DSurface` class, a DirectDraw-based surface implementation for rendering operations in the game engine.

## Responsibilities
- Manages DirectDraw surfaces for rendering
- Provides blitting, locking, and filling operations
- Handles device context management for GDI interop
- Tracks surface memory location (system/Video RAM)
- Maintains pixel format and color conversion utilities

## Key Types
- **DSurface (Class)**: DirectDraw surface wrapper with rendering capabilities
- **BASECLASS (Class)**: Alias for XSurface (base class)
- **None**: No enums/structs defined

## Key Functions
### DSurface::Create_Primary
- Purpose: Creates a primary surface representing the visible screen
- Calls: Not inferable

### DSurface::Blit_From
- Purpose: Copies regions between surfaces with optional transparency
- Calls: XSurface::Blit_From

### DSurface::Lock/Unlock
- Purpose: Locks/unlocks surface memory for direct access
- Calls: Not inferable

### DSurface::Build_Hicolor_Pixel
- Purpose: Constructs a high-color pixel from RGB components
- Calls: Not inferable

### DSurface::Build_Remap_Table
- Purpose: Builds a color remapping table for palette operations
- Calls: Not inferable

## Globals
- **Clipper (LPDIRECTDRAWCLIPPER)**: Static clipper for primary surface
- **PixelFormat (DDPIXELFORMAT)**: Primary surface pixel format
- **RedRight/RedLeft/BlueRight/BlueLeft/GreenRight/GreenLeft (int)**: Color channel shift values
- **ThisRedRight/ThisRedLeft/ThisBlueRight/ThisBlueLeft/ThisGreenRight/ThisGreenLeft (int)**: Surface-specific color shifts
- **HalfbrightMask/QuarterbrightMask/EighthbrightMask (unsigned short)**: Precomputed brightness masks

## Dependencies
- `palette.h`, `win.h`, `xsurface.h`, `ddraw.h`
- `XSurface` base class
- DirectDraw API types (`LPDIRECTDRAWSURFACE`, `DDSURFACEDESC`, etc.)
- Windows GDI types (`HDC`)
