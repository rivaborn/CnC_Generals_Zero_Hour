# Generals/Code/Libraries/Source/WWVegas/WWMath/vector4.h

## Purpose
Defines a 4D vector class with mathematical operations for 3D/4D vector manipulation.

## Responsibilities
- Provides 4D vector storage and arithmetic
- Implements vector normalization, dot product, and interpolation
- Supports scalar and vector operations
- Includes validation checks for vector components

## Key Types
- Vector4 (Class): 4D vector with X, Y, Z, W components and mathematical operations

## Key Functions
### operator* (Vector4, float)
- Purpose: Scalar multiplication of a vector
- Calls: None

### operator* (float, Vector4)
- Purpose: Scalar multiplication (commutative form)
- Calls: operator* (Vector4, float)

### operator+ (Vector4, Vector4)
- Purpose: Vector addition
- Calls: None

### operator- (Vector4, Vector4)
- Purpose: Vector subtraction
- Calls: None

### operator* (Vector4, Vector4)
- Purpose: Dot product calculation
- Calls: None

### Normalize (Vector4)
- Purpose: Returns normalized vector
- Calls: Length2(), WWMath::Inv_Sqrt()

### Swap (Vector4&, Vector4&)
- Purpose: Swaps two vectors
- Calls: None

### Lerp (Vector4, Vector4, float)
- Purpose: Linear interpolation between vectors
- Calls: None

## Globals
- None

## Dependencies
- "always.h", "wwmath.h", <math.h>
- WWMath::Inv_Sqrt(), WWMath::Sqrt(), WWMath::Is_Valid_Float()
