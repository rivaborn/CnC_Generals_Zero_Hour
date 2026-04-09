# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vector2.h

## Purpose
Defines a 2D vector class with mathematical operations for game physics and geometry.

## Responsibilities
- Provides 2D vector arithmetic (addition, subtraction, dot product)
- Supports vector normalization, rotation, and interpolation
- Implements distance calculations and vector comparisons
- Manages vector component access and validation

## Key Types
- Vector2 (Class): 2D mathematical vector with X/Y components
- (anonymous union) (Class): Allows X/U and Y/V component naming
- (anonymous union) (Class): Allows X/U and Y/V component naming

## Key Functions
### operator* (scalar multiplication)
- Purpose: Multiplies vector by scalar
- Calls: None

### operator+ (vector addition)
- Purpose: Adds two vectors
- Calls: None

### operator- (vector subtraction)
- Purpose: Subtracts two vectors
- Calls: None

### Normalize
- Purpose: Normalizes vector to unit length
- Calls: Length2, WWMath::Inv_Sqrt

### Quick_Distance
- Purpose: Fast approximate distance calculation
- Calls: WWMath::Fabs

### Distance
- Purpose: Accurate Euclidean distance between vectors
- Calls: Length

### Lerp
- Purpose: Linear interpolation between two vectors
- Calls: None

## Globals
- None

## Dependencies
- "always.h", "wwmath.h", <math.h>
- WWMath::Fabs, WWMath::Inv_Sqrt, WWMath::Sqrt, WWMath::Is_Valid_Float
- assert (for Lerp validation)
