# GeneralsMD/Code/Libraries/Include/Lib/BaseType.h

## Purpose
Defines fundamental data types, mathematical utilities, and spatial structures used throughout the game engine.

## Responsibilities
- Declares basic numeric types (Real, Int, etc.)
- Provides 2D/3D coordinate and region structures
- Implements math utilities (clamp, sqr, trig functions)
- Defines color types (RGB, RGBA)
- Contains fast floating-point conversion routines

## Key Types
- **Real (typedef)**: 4-byte floating-point number
- **Coord2D (struct)**: 2D vector with length/normalize operations
- **Coord3D (struct)**: 3D vector with cross product, normalization
- **Region3D (struct)**: Axis-aligned bounding box with containment checks
- **RGBColor (struct)**: Color with 0-1 range components
- **RealRange (struct)**: Numeric range with combination logic

## Key Functions
### sqr
- Purpose: Returns square of input value
- Calls: None

### clamp
- Purpose: Clamps value between low and high bounds
- Calls: None

### fast_float2long_round
- Purpose: Fast floating-point to integer conversion with rounding
- Calls: None (uses inline assembly)

### Coord3D::normalize
- Purpose: Normalizes 3D vector to unit length
- Calls: length()

### Region3D::isInRegionWithZ
- Purpose: Checks if point is within 3D region bounds
- Calls: None

## Globals
- **PI (const)**: Mathematical constant Ï
- **TWO_PI (const)**: 2Ï constant
- Bit manipulation macros (BitTest, BitSet, etc.)

## Dependencies
- `<math.h>` for sqrt, trig functions
- `<string.h>` for memory operations
- "Lib/Trig.h" for angle conversion utilities
- Uses inline assembly for fast float operations
