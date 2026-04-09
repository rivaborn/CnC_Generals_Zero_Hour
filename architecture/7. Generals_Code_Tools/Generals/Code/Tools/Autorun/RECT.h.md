# Generals/Code/Tools/Autorun/RECT.h

## Purpose
Defines a generic rectangle class and utility functions for rectangle operations.

## Responsibilities
- Provides a templated rectangle class (`TRect`) for 2D spatial operations
- Implements rectangle union and intersection logic
- Supports point-in-rectangle and rectangle-overlap tests
- Manages rectangle validity and clipping operations

## Key Types
- **TRect<T> (Class)**: Generic rectangle class with position (X,Y) and dimensions (Width,Height)
- **Rect (Class)**: Integer specialization of TRect
- **RECT_NONE (const Rect)**: Invalid rectangle constant (0,0,0,0)

## Key Functions
### Union
- Purpose: Combines two rectangles into the smallest enclosing rectangle
- Calls: `Is_Valid()`

### Intersect (bounding_rect, draw_rect, x, y)
- Purpose: Computes intersection with clipping offsets
- Calls: `Is_Valid()`

### Intersect (rect1, rect2)
- Purpose: Computes simple intersection of two rectangles
- Calls: `Intersect(bounding_rect, draw_rect, NULL, NULL)`

### Bias_To (point, rect)
- Purpose: Adjusts a point relative to a rectangle's origin
- Calls: None

## Globals
- **RECT_NONE (const Rect)**: Invalid rectangle constant

## Dependencies
- `point.h` (for `TPoint2D`)
- Standard C++ template mechanisms
