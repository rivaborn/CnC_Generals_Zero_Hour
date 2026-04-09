# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/xsurface.h

## Purpose
Defines the `XSurface` class, a concrete implementation of the `Surface` base class for handling pixel-based surface operations without hardware acceleration.

## Responsibilities
- Provides methods for blitting, filling, drawing primitives, and pixel manipulation
- Manages surface locking/unlocking for direct memory access
- Offers utility functions for surface preparation and clipping
- Abstracts low-level surface operations for portability

## Key Types
- **XSurface (Class)**: Concrete surface implementation for CPU-based pixel operations
- **Blit_Clip (Function)**: Helper for clipping rectangles during blit operations

## Key Functions
### Blit_From (3 overloads)
- Purpose: Copies regions between surfaces with optional transparency
- Calls: Not inferable (implementation in .cpp)

### Fill_Rect (3 overloads)
- Purpose: Fills rectangular regions with a solid color
- Calls: Not inferable

### Draw_Line (2 overloads)
- Purpose: Draws lines between two points with clipping support
- Calls: Not inferable

### Draw_Rect (2 overloads)
- Purpose: Draws rectangles with optional clipping
- Calls: Not inferable

### Prep_For_Blit (2 overloads)
- Purpose: Prepares surfaces and rectangles for manual blit operations
- Calls: Not inferable

### Blit_Trans / Blit_Plain
- Purpose: Manual blit implementations for transparency and plain copies
- Calls: Not inferable

## Globals
- **None**

## Dependencies
- `surface.h` (base class)
- `Rect`, `Point2D` (geometry types)
- Assumes pixel data stored in contiguous linear array
