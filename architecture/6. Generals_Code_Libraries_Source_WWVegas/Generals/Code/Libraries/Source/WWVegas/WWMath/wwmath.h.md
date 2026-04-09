# Generals/Code/Libraries/Source/WWVegas/WWMath/wwmath.h

## Purpose
Header file defining the WWMath class, providing optimized math utilities for the SAGE engine.

## Responsibilities
- Provides fast math operations (trig, sqrt, etc.)
- Includes table-based approximations for performance
- Handles float conversions and clamping
- Supports platform-specific optimizations (x86 assembly)
- Manages math initialization/shutdown

## Key Types
- WWMath (Class): Central math utility class with static methods

## Key Functions
### WWMath::Init
- Purpose: Initialize math subsystem
- Calls: Not inferable

### WWMath::Shutdown
- Purpose: Clean up math subsystem
- Calls: Not inferable

### WWMath::Fabs
- Purpose: Absolute value for floats
- Calls: None

### WWMath::Fast_Sin/Fast_Cos
- Purpose: Table-based fast trigonometric functions
- Calls: Uses _FastSinTable, Float_To_Int_Floor

### WWMath::Inv_Sqrt
- Purpose: Fast inverse square root (x86 assembly optimized)
- Calls: None

### WWMath::Clamp/Wrap
- Purpose: Value range management
- Calls: None

### WWMath::Is_Valid_Float/Is_Valid_Double
- Purpose: Float validity checking
- Calls: None

## Globals
- ARC_TABLE_SIZE (int): Size constant for arc tables
- SIN_TABLE_SIZE (int): Size constant for sine tables
- _FastAcosTable (float[]): Precomputed acos values
- _FastAsinTable (float[]): Precomputed asin values
- _FastSinTable (float[]): Precomputed sine values
- _FastInvSinTable (float[]): Precomputed 1/sin values

## Dependencies
- <math.h>, <float.h>, <assert.h>
- always.h (for WWINLINE)
- Platform-specific x86 assembly for optimizations
- Uses reinterpret_cast for float/int conversions
