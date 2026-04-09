# Generals/Code/Tools/WW3D/pluglib/wwmath.h

## Purpose
Provides basic mathematical utilities for the WW3D plugin library, including floating-point operations, clamping, wrapping, and random number generation.

## Responsibilities
- Provides static math utility functions (e.g., Fabs, Sqrt, Clamp)
- Implements floating-point validation (Is_Valid_Float/Is_Valid_Double)
- Handles float-to-integer conversions (Float_To_Long)
- Supports degree/radian conversions via macros
- Includes fast math operations (e.g., Inv_Sqrt, Fast_Is_Float_Positive)

## Key Types
- **WWMath (Class)**: Static utility class for mathematical operations.

## Key Functions
### WWMath::Sign
- Purpose: Returns the sign of a float (+1, -1, or 0).
- Calls: None.

### WWMath::Fast_Is_Float_Positive
- Purpose: Checks if a float is positive using bitwise operations.
- Calls: None.

### WWMath::Random_Float
- Purpose: Generates a random float in [0,1) or [min,max).
- Calls: None (assumes external RNG).

### WWMath::Clamp
- Purpose: Clamps a value between min and max.
- Calls: None.

### WWMath::Wrap
- Purpose: Wraps a value within [min,max) bounds.
- Calls: None.

### WWMath::Lerp
- Purpose: Linearly interpolates between two values.
- Calls: None.

### WWMath::Float_To_Long
- Purpose: Converts a float/double to a long (uses x86 assembly for speed).
- Calls: None.

### WWMath::Is_Valid_Float/Is_Valid_Double
- Purpose: Checks for NaN values in floats/doubles.
- Calls: None.

## Globals
- **WWMATH_EPSILON (float)**: Small epsilon value for floating-point comparisons.
- **WWMATH_PI (float)**: Pi constant.
- **WWMATH_FLOAT_MAX (float)**: Maximum representable float.
- **WWMATH_SQRT2/SQRT3 (float)**: Square root constants.
- **RAD_TO_DEG/DEG_TO_RAD (macros)**: Degree/radian conversion macros.

## Dependencies
- `<math.h>`: For `fabs`, `sqrt`, `floor`.
- `<assert.h>`: For assertions.
- `always.h`: Likely for platform-specific macros.
- Uses x86-specific assembly for `Float_To_Long` (MSVC only).
