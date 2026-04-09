# Generals/Code/Tools/WW3D/pluglib/vector2.h

## Purpose
Defines a 2D vector class with mathematical operations and utilities for the SAGE engine.

## Responsibilities
- Provides 2D vector arithmetic (addition, subtraction, dot product, etc.)
- Supports vector normalization, rotation, and distance calculations
- Implements comparison operators and epsilon-based equality checks
- Offers utility functions like min/max updates and linear interpolation

## Key Types
- **Vector2 (Class)**: 2D vector with X/Y components (also accessible as U/V)
- **(anonymous union) (Class)**: Allows X/U and Y/V component naming
- **(anonymous union) (Class)**: Allows X/U and Y/V component naming

## Key Functions
### `operator * (const Vector2 &a, float k)`
- Purpose: Scalar multiplication of a vector
- Calls: None

### `operator + (const Vector2 &a, const Vector2 &b)`
- Purpose: Vector addition
- Calls: None

### `operator - (const Vector2 &a, const Vector2 &b)`
- Purpose: Vector subtraction
- Calls: None

### `Normalize()`
- Purpose: Normalizes the vector to unit length
- Calls: `Length2()`, `WWMath::Inv_Sqrt()`

### `Rotate(float theta)`
- Purpose: Rotates the vector by an angle
- Calls: `Rotate(s, c)`

### `Rotate_Towards_Vector(Vector2 &target, float max_theta, bool &positive_turn)`
- Purpose: Rotates towards a target vector with a maximum angle
- Calls: `Rotate_Towards_Vector(target, max_s, max_c, positive_turn)`

### `Quick_Distance(const Vector2 &a, const Vector2 &b)`
- Purpose: Fast but approximate distance calculation
- Calls: `::Quick_Distance(a.X, a.Y, b.X, b.Y)`

### `Distance(const Vector2 &a, const Vector2 &b)`
- Purpose: Accurate Euclidean distance calculation
- Calls: `Length()`

## Globals
- None

## Dependencies
- `always.h`, `wwmath.h`, `<math.h>`
- `WWMath::Fabs()`, `WWMath::Sqrt()`, `WWMath::Inv_Sqrt()`, `WWMath::Is_Valid_Float()`
