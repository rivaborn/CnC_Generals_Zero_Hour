# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/aabox.cpp

## Purpose
Implements axis-aligned bounding box (AABB) functionality for collision detection and spatial queries.

## Responsibilities
- Initializes AABBs with random or empty states
- Tests containment of points and other AABBs
- Transforms AABBs using 3D matrices

## Key Types
- **AABoxClass**: Represents an axis-aligned bounding box with center and extent.
- **MinMaxAABoxClass**: Represents an AABB defined by min/max corners.

## Key Functions
### AABoxClass::Init_Random
- Purpose: Initializes an AABB with random center and extent values.
- Calls: `WWMath::Random_Float()`

### AABoxClass::Transform
- Purpose: Transforms an input AABB using a 3D matrix and stores result in output.
- Calls: `Matrix3D::Transform_Center_Extent_AABox()`

### MinMaxAABoxClass::Init_Empty
- Purpose: Initializes an empty AABB with extreme min/max values.
- Calls: None

## Globals
- None

## Dependencies
- `aabox.h`, `colmath.h`, `colmathinlines.h`, `<float.h>`
- `WWMath::Random_Float()`, `Matrix3D::Transform_Center_Extent_AABox()`
