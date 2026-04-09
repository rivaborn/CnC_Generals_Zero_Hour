# Generals/Code/Libraries/Source/WWVegas/WWMath/vector3.h

## Purpose
Defines a 3D vector class with mathematical operations for 3D spatial calculations.

## Responsibilities
- Provides 3D vector arithmetic (addition, subtraction, dot/cross products)
- Supports vector normalization, length calculations, and rotations
- Implements comparison operations and epsilon-based equality checks
- Includes utility functions for interpolation, distance, and coordinate conversions

## Key Types
- Vector3 (Class): 3D vector with x,y,z components and mathematical operations

## Key Functions
### operator* (scalar multiplication)
- Purpose: Multiply vector by scalar
- Calls: None

### operator+ (vector addition)
- Purpose: Add two vectors
- Calls: None

### operator- (vector subtraction)
- Purpose: Subtract two vectors
- Calls: None

### Dot_Product
- Purpose: Compute dot product of two vectors
- Calls: None

### Cross_Product
- Purpose: Compute cross product of two vectors
- Calls: None

### Lerp
- Purpose: Linearly interpolate between two vectors
- Calls: None

### Normalize
- Purpose: Normalize vector to unit length
- Calls: None

## Globals
None

## Dependencies
- "always.h", "wwmath.h", <assert.h>
- WWMath::Fabs, WWMath::Is_Valid_Float
- sinf, cosf (math library)
