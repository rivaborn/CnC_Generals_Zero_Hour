# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vector3.h

## Purpose
Defines a 3D vector class with mathematical operations for 3D spatial calculations.

## Responsibilities
- Provides 3D vector arithmetic (addition, subtraction, dot/cross products)
- Supports vector normalization, rotation, and interpolation
- Implements comparison operations with epsilon tolerance
- Handles vector-scalar operations and coordinate transformations

## Key Types
- Vector3 (Class): 3D vector with x,y,z components and mathematical operations

## Key Functions
### operator* (vector-scalar)
- Purpose: Multiplies vector by scalar
- Calls: None

### operator+ (vector addition)
- Purpose: Adds two vectors
- Calls: None

### operator- (vector subtraction)
- Purpose: Subtracts two vectors
- Calls: None

### Dot_Product
- Purpose: Computes dot product of two vectors
- Calls: None

### Cross_Product
- Purpose: Computes cross product of two vectors
- Calls: None

### Normalize
- Purpose: Normalizes vector to unit length
- Calls: None

### Lerp
- Purpose: Linearly interpolates between two vectors
- Calls: None

### Swap
- Purpose: Swaps contents of two vectors
- Calls: None

## Globals
None

## Dependencies
- "always.h", "wwmath.h", <assert.h>
- WWMath::Fabs, WWMath::Is_Valid_Float
- sinf, cosf (math library)
