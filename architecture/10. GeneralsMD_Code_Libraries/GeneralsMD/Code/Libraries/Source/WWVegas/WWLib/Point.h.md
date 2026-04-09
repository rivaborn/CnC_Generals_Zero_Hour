# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Point.h

## Purpose
Defines 2D and 3D point/vector classes with arithmetic and geometric operations.

## Responsibilities
- Provides template-based 2D and 3D point/vector classes
- Implements vector math operations (addition, subtraction, dot/cross products)
- Supports normalization, length calculation, and distance measurement
- Includes scalar multiplication/division and point biasing

## Key Types
- TPoint2D (Class): 2D point/vector with X,Y components
- TPoint3D (Class): 3D point/vector inheriting from TPoint2D with Z component
- Point2D (Typedef): Integer specialization of TPoint2D
- Point3D (Typedef): Integer specialization of TPoint3D
- TRect (Forward declaration): Used for point biasing

## Key Functions
### operator* (T, TPoint2D)
- Purpose: Scalar multiplication for TPoint2D
- Calls: TPoint2D::operator*

### operator* (T, TPoint3D)
- Purpose: Scalar multiplication for TPoint3D
- Calls: TPoint3D::operator*

## Globals
None

## Dependencies
- `<cmath>` (for sqrt)
- TRect template class (forward declared)
