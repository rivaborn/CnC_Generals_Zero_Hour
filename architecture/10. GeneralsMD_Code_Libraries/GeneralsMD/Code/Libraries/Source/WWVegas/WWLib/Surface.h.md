# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Surface.h

## Purpose
Defines an abstract interface class for graphic surfaces, providing basic drawing and pixel manipulation operations.

## Responsibilities
- Declares pure virtual methods for surface operations (blitting, filling, drawing).
- Provides accessors for surface properties (dimensions, pixel format).
- Supports memory locking/unlocking for direct access.
- Includes a workaround for RTTI (Is_Direct_Draw).

## Key Types
- **Surface (Class)**: Abstract base class for graphic surfaces.

## Key Functions
### Surface::Blit_From
- Purpose: Copies regions between surfaces.
- Calls: None (pure virtual).

### Surface::Fill_Rect
- Purpose: Fills a region with a constant color.
- Calls: None (pure virtual).

### Surface::Draw_Line
- Purpose: Draws a line between two points.
- Calls: None (pure virtual).

### Surface::Lock
- Purpose: Locks surface memory for direct access.
- Calls: None (pure virtual).

## Globals
- None.

## Dependencies
- `Point.h`, `TRect.h` (included).
- `Point2D`, `Rect` (used in method signatures).
