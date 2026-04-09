# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/surfrect.h

## Purpose
Header file defining a `SurfaceRect` class that combines a surface and a clipping rectangle for convenience in rendering operations.

## Responsibilities
- Encapsulate a surface and a clipping rectangle.
- Provide constructors for initialization with different parameters.
- Track a 2D coordinate within the surface.
- Prevent copy construction and assignment.

## Key Types
- **SurfaceRect (Class)**: Combines a surface pointer, a clipping rectangle, and a 2D point for surface operations.
- **Surface * (Type)**: Pointer to the surface being referenced.
- **Rect (Type)**: Clipping rectangle within the surface.
- **Point2D (Type)**: 2D coordinate within the surface.

## Key Functions
### SurfaceRect (Constructors)
- Purpose: Initialize a `SurfaceRect` with a surface and optional clipping rectangle.
- Calls: `SurfacePtr->Get_Rect()` (in some constructors).

## Globals
- None

## Dependencies
- `surface.h` (Surface class)
- `trect.h` (Rect class)
- `point.h` (Point2D class)
- `<assert.h>` (assert macro)
