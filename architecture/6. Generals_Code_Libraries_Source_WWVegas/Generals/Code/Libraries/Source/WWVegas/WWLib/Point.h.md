# Generals/Code/Libraries/Source/WWVegas/WWLib/Point.h

## Purpose
Defines 2D and 3D point/vector classes with arithmetic and geometric operations.

## Responsibilities
- Provides template-based 2D and 3D point/vector classes
- Implements vector math operations (addition, subtraction, dot/cross products)
- Supports normalization, length calculation, and distance measurement
- Includes scalar multiplication/division and point biasing

## Key Types
- TPoint2D (Class): 2D point/vector with X,Y components
- Point2D (Class): Typedef for int-based TPoint2D
- TPoint3D (Class): 3D point/vector inheriting from TPoint2D, adding Z component
- Point3D (Class): Typedef for int-based TPoint3D
- BASECLASS (Class): Inheritance reference for TPoint3D

## Key Functions
### operator* (T lvalue, TPoint2D<T> const & rvalue)
- Purpose: Scalar multiplication for TPoint2D
- Calls: rvalue * lvalue

### operator* (T lvalue, TPoint3D<T> const & rvalue)
- Purpose: Scalar multiplication for TPoint3D
- Calls: rvalue * lvalue

## Globals
None

## Dependencies
- TRect template class (forward declared)
- Standard math functions (sqrt)
