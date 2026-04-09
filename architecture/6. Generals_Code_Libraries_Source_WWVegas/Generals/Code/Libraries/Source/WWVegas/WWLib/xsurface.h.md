# Generals/Code/Libraries/Source/WWVegas/WWLib/xsurface.h

## Purpose
Defines the `XSurface` class, a concrete implementation of the `Surface` base class for handling pixel-based surface operations without hardware acceleration.

## Responsibilities
- Provides methods for blitting, filling, drawing primitives, and pixel manipulation.
- Manages surface locking/unlocking for direct memory access.
- Offers utility functions for surface preparation and clipping.

## Key Types
- **XSurface (Class)**: Concrete surface implementation for pixel-based operations.
- **Blit_Clip (Function)**: Helper for clipping rectangles during blit operations.

## Key Functions
### Blit_From (3 overloads)
- Purpose: Copies regions between surfaces with optional transparency.
- Calls: Not inferable (implementation in .cpp).

### Fill_Rect (3 overloads)
- Purpose: Fills rectangles or the entire surface with a color.
- Calls: Not inferable.

### Draw_Line (2 overloads)
- Purpose: Draws lines on the surface with clipping support.
- Calls: Not inferable.

### Draw_Rect (2 overloads)
- Purpose: Draws rectangles with clipping support.
- Calls: Not inferable.

### Prep_For_Blit (2 overloads)
- Purpose: Prepares surfaces and rectangles for manual blit operations.
- Calls: Not inferable.

### Blit_Trans / Blit_Plain
- Purpose: Manual blit routines for transparency and plain copies.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `surface.h` (base class `Surface`).
- External types: `Rect`, `Point2D`.
