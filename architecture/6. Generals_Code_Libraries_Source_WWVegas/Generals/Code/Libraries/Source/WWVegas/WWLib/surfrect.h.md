# Generals/Code/Libraries/Source/WWVegas/WWLib/surfrect.h

## Purpose
Header file defining a `SurfaceRect` class that combines a surface and a clipping rectangle for convenience in rendering operations.

## Responsibilities
- Encapsulate a surface and a clipping rectangle.
- Provide constructors for initialization with different parameters.
- Track a 2D coordinate within the surface.
- Prevent copy construction and assignment.

## Key Types
- **SurfaceRect (Class)**: Encapsulates a surface and a clipping rectangle for rendering operations.

## Key Functions
### SurfaceRect (Constructors)
- Purpose: Initialize a `SurfaceRect` with a surface and optionally a clipping rectangle.
- Calls: `Surface::Get_Rect()` (indirectly via constructor logic).

## Globals
- None

## Dependencies
- `surface.h` (Surface class)
- `trect.h` (Rect class)
- `point.h` (Point2D class)
- `<assert.h>` (assert macro)
