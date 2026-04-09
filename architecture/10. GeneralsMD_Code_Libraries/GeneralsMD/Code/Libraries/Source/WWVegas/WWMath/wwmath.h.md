# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/wwmath.h

## Purpose
Header file defining the WWMath class, providing optimized math utilities for the SAGE engine.

## Responsibilities
- Provides fast math operations (trigonometry, square roots, etc.)
- Includes initialization/shutdown for math subsystems
- Offers utility functions (clamping, wrapping, random number generation)
- Supports both precise and fast (table-based) math operations
- Handles float/int conversions and validation

## Key Types
- **WWMath (Class)**: Central math utility class with static methods for various operations

## Key Functions
### WWMath::Init
- Purpose: Initialize math subsystem
- Calls: None

### WWMath::Shutdown
- Purpose: Shutdown math subsystem
- Calls: None

### WWMath::Fabs
- Purpose: Absolute value for floats
- Calls: None

### WWMath::Fast_Sin
- Purpose: Fast sine using lookup tables
- Calls: Float_To_Int_Floor

### WWMath::Inv_Sqrt
- Purpose: Fast inverse square root (Intel assembly optimized)
- Calls: None

### WWMath::Clamp
- Purpose: Clamp float value between min/max
- Calls: None

### WWMath::Is_Valid_Float
- Purpose: Check if float is valid (not NaN)
- Calls: None

## Globals
- **ARC_TABLE_SIZE (int)**: Size of arc function lookup tables
- **SIN_TABLE_SIZE (int)**: Size of sine/cosine lookup tables
- **_FastAcosTable (float[])**: Precomputed acos values
- **_FastAsinTable (float[])**: Precomputed asin values
- **_FastSinTable (float[])**: Precomputed sine values
- **_FastInvSinTable (float[])**: Precomputed 1/sine values

## Dependencies
- Key includes: `always.h`, `math.h`, `float.h`, `assert.h`
- External symbols: `WWMATH_PI`, `WWMATH_EPSILON`, `WWINLINE` macros
- Uses inline assembly for x86 optimizations
