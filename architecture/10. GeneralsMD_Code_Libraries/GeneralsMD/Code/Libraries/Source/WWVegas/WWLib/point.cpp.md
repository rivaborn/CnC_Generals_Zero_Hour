# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/point.cpp

## Purpose
Implements the `Point2D::Bias_To` method for biasing a point into a rectangle's coordinate space.

## Responsibilities
- Provides point-to-rectangle coordinate transformation
- Handles relative-to-absolute coordinate conversion
- Supports 2D point operations

## Key Types
- `Point2D` (Class): Represents a 2D point with X/Y coordinates
- `Rect` (Class): Represents a rectangle (used for biasing)

## Key Functions
### `Point2D::Bias_To`
- Purpose: Transforms a point into a rectangle's coordinate space while maintaining the same location
- Calls: None (simple arithmetic)

## Globals
- None

## Dependencies
- `always.h` (header)
- `point.h` (header)
- `rect.h` (header)
- `Point2D` class (external)
- `Rect` class (external)
