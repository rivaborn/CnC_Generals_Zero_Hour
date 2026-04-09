# Generals/Code/Libraries/Source/WWVegas/WWMath/vector2.h

## Purpose
Defines a 2D vector class with mathematical operations for vector manipulation in the game engine.

## Responsibilities
- Provides 2D vector arithmetic (addition, subtraction, dot product, etc.)
- Supports vector normalization, rotation, and distance calculations
- Implements comparison operations with epsilon tolerance
- Offers utility functions like min/max updates and linear interpolation

## Key Types
- **Vector2 (Class)**: 2D vector with X/Y components supporting various mathematical operations
- **(anonymous union)**: Allows accessing X/Y components via U/V aliases
- **None**: No enums or other structs

## Key Functions
### `operator*` (scalar multiplication)
- Purpose: Multiplies a vector by a scalar value
- Calls: None

### `operator+` (vector addition)
- Purpose: Adds two vectors component-wise
- Calls: None

### `Normalize()`
- Purpose: Normalizes the vector to unit length
- Calls: `Length2()`, `WWMath::Inv_Sqrt()`

### `Rotate_Towards_Vector()`
- Purpose: Rotates the vector toward a target vector with angle constraints
- Calls: `Dot_Product()`, `Perp_Dot_Product()`, `Rotate()`

### `Quick_Distance()`
- Purpose: Computes an approximate distance between two vectors (faster but less accurate)
- Calls: `WWMath::Fabs()`

### `Lerp()`
- Purpose: Linearly interpolates between two vectors
- Calls: None

## Globals
- **None**: No global/static variables

## Dependencies
- `always.h`, `wwmath.h`, `<math.h>`
- `WWMath` namespace functions (`Fabs`, `Sqrt`, `Inv_Sqrt`, `Is_Valid_Float`)
- `assert()` for debug checks
