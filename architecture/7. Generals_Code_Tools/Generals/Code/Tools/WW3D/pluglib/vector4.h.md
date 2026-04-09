# Generals/Code/Tools/WW3D/pluglib/vector4.h

## Purpose
Defines a 4D vector class with mathematical operations for 3D/4D vector manipulation.

## Responsibilities
- Provides 4D vector arithmetic (addition, subtraction, dot product)
- Supports scalar multiplication/division
- Implements vector normalization and length calculation
- Includes interpolation (Lerp) and validation utilities

## Key Types
- **Vector4 (Class)**: 4D vector with X,Y,Z,W components and vector operations

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

## Globals
- None

## Dependencies
- `always.h`, `wwmath.h`, `<math.h>`
- `WWMath::Inv_Sqrt`, `WWMath::Sqrt`, `WWMath::Is_Valid_Float`
