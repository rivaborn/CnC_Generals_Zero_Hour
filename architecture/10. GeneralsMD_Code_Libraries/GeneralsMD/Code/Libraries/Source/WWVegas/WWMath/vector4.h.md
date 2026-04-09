# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vector4.h

## Purpose
Defines a 4D vector class with mathematical operations for 3D/4D vector manipulation.

## Responsibilities
- Provides 4D vector storage and arithmetic
- Implements vector normalization, length calculation, and dot product
- Supports linear interpolation (lerp) between vectors
- Includes vector comparison and validation utilities

## Key Types
- **Vector4 (Class)**: 4D vector with x,y,z,w components and mathematical operations

## Key Functions
### `operator*` (scalar multiplication)
- Purpose: Multiply vector by scalar
- Calls: None

### `operator+` (vector addition)
- Purpose: Add two vectors
- Calls: None

### `operator-` (vector subtraction)
- Purpose: Subtract two vectors
- Calls: None

### `Normalize`
- Purpose: Normalize vector to unit length
- Calls: `Length2()`, `WWMath::Inv_Sqrt`

### `Lerp`
- Purpose: Linearly interpolate between two vectors
- Calls: None

### `Swap`
- Purpose: Swap contents of two vectors
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `wwmath.h`, `<math.h>`
- `WWMath::Inv_Sqrt`, `WWMath::Sqrt`, `WWMath::Is_Valid_Float`
