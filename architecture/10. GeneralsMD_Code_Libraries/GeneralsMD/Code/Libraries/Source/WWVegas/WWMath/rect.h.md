# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/rect.h

## Purpose
Defines a 2D rectangular region class with geometric operations.

## Responsibilities
- Represents a rectangle with left, top, right, bottom edges
- Provides scaling, translation, and containment operations
- Supports union and inflation of rectangles
- Offers coordinate snapping and center/extent calculations

## Key Types
- **RectClass (Class)**: 2D axis-aligned rectangle with geometric operations

## Key Functions
### RectClass::Scale_Relative_Center
- Purpose: Scales rectangle relative to its center point
- Calls: Center(), operator-=, operator+=

### RectClass::Contains
- Purpose: Checks if a point is inside the rectangle
- Calls: None

### RectClass::Snap_To_Units
- Purpose: Snaps rectangle edges to grid units
- Calls: None

## Globals
- None

## Dependencies
- `vector2.h` (Vector2 class)
- MIN/MAX macros (for union operation)
