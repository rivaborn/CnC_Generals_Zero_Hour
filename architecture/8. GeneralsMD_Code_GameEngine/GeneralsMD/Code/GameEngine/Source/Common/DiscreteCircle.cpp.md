# GeneralsMD/Code/GameEngine/Source/Common/DiscreteCircle.cpp

## Purpose
Implements a discrete circle using Bresenham's algorithm for rendering scanlines.

## Responsibilities
- Generates horizontal line segments (edges) for a circle.
- Removes duplicate edges.
- Provides a draw function to render the circle via a callback.

## Key Types
- `DiscreteCircle` (Class): Manages circle edge generation and rendering.
- `HorzLine` (Struct): Represents a horizontal line segment (xStart, xEnd, yPos).
- `VecHorzLine` (Type): Container for `HorzLine` objects.

## Key Functions
### `DiscreteCircle::DiscreteCircle(Int xCenter, Int yCenter, Int radius)`
- Purpose: Constructs a discrete circle with given center and radius.
- Calls: `generateEdgePairs`, `removeDuplicates`.

### `DiscreteCircle::drawCircle(ScanlineDrawFunc functionToDrawWith, void *parmToPass)`
- Purpose: Renders the circle by invoking a callback for each edge.
- Calls: `functionToDrawWith` (callback).

### `DiscreteCircle::generateEdgePairs(Int xCenter, Int yCenter, Int radius)`
- Purpose: Generates circle edges using Bresenham's algorithm.
- Calls: None.

### `DiscreteCircle::removeDuplicates()`
- Purpose: Removes duplicate horizontal edges.
- Calls: None.

## Globals
None.

## Dependencies
- `Common/DiscreteCircle.h` (header)
- `PreRTS.h` (precompiled header)
- `ScanlineDrawFunc` (callback type)
