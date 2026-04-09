# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/trect.h

## Purpose
Defines a templated rectangle class for 2D spatial operations, supporting intersection, union, and point containment checks.

## Responsibilities
- Manages rectangle geometry (position, dimensions)
- Provides spatial operations (intersection, union, overlap)
- Supports point containment and rectangle validity checks
- Offers arithmetic operations with points

## Key Types
- **TRect<T> (Class)**: Templated rectangle with position (X,Y) and dimensions (Width,Height)
- **Rect (Typedef)**: Integer specialization of TRect

## Key Functions
### TRect<T>::Intersect
- Purpose: Computes intersection with another rectangle.
- Calls: Is_Valid()

### TRect<T>::Union
- Purpose: Computes union with another rectangle.
- Calls: Is_Valid()

### TRect<T>::Is_Overlapping
- Purpose: Checks if two rectangles overlap.
- Calls: None

### TRect<T>::Is_Point_Within
- Purpose: Checks if a point lies within the rectangle.
- Calls: None

## Globals
- None

## Dependencies
- **point.h**: For TPoint2D<T> usage
- External: None defined here
