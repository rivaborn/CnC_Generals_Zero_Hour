# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/xsurface.cpp

## Purpose
Implements surface rendering operations for the SAGE engine, including blitting, drawing primitives, and pixel manipulation.

## Responsibilities
- Surface blitting (with/without transparency)
- Drawing lines, rectangles, and fills
- Pixel-level operations (get/put)
- Clipping rectangle management
- Surface locking/unlocking for memory access

## Key Types
- `XSurface` (Class): Surface rendering operations
- `Rect` (Struct): Rectangle definition
- `Point2D` (Struct): 2D point coordinates
- `Blit_Clip` (Function): Rectangle clipping utility

## Key Functions
### `Blit_Clip`
- Purpose: Perform rectangle clipping for blit operations
- Calls: None

### `XSurface::Blit_From`
- Purpose: Blit from one surface to another with clipping
- Calls: `Blit_Clip`, `Blit_Trans`, `Blit_Plain`

### `XSurface::Draw_Line`
- Purpose: Draw a line on the surface
- Calls: `Lock`, `Unlock`

### `XSurface::Fill_Rect`
- Purpose: Fill a rectangle with a color
- Calls: `Lock`, `Unlock`

### `XSurface::Blit_Plain`
- Purpose: Perform a simple blit operation
- Calls: `Bit_Blit`

### `XSurface::Blit_Trans`
- Purpose: Perform a transparent blit operation
- Calls: `Bit_Blit`

## Globals
None

## Dependencies
- `blit.h`, `blitblit.h`, `bsurface.h`, `swap.h`, `xsurface.h`
- `Rect`, `Point2D`, `Surface` classes
- `Bit_Blit`, `BlitPlain`, `BlitTrans` templates
