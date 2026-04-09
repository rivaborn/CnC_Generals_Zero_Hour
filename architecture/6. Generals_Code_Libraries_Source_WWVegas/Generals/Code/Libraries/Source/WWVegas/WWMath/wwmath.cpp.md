# Generals/Code/Libraries/Source/WWVegas/WWMath/wwmath.cpp

## Purpose
Initializes and manages mathematical lookup tables and utilities for the game engine.

## Responsibilities
- Initializes trigonometric lookup tables (sin, asin, acos, inverse sin).
- Provides random float generation.
- Manages module linking for math-related libraries.
- Handles engine startup/shutdown for math components.

## Key Types
- None

## Key Functions
### WWMath::Init
- Purpose: Initializes lookup tables and math utilities.
- Calls: `LookupTableMgrClass::Init`, `acos`, `asin`, `sin`

### WWMath::Shutdown
- Purpose: Cleans up math utilities.
- Calls: `LookupTableMgrClass::Shutdown`

### WWMath::Random_Float
- Purpose: Generates a random float between 0 and 1.
- Calls: `rand`

### Do_Force_Links
- Purpose: Forces linking of math-related modules.
- Calls: `FORCE_LINK` (macro)

## Globals
- `_FastAcosTable` (float[]): Precomputed acos values.
- `_FastAsinTable` (float[]): Precomputed asin values.
- `_FastSinTable` (float[]): Precomputed sin values.
- `_FastInvSinTable` (float[]): Precomputed inverse sin values.

## Dependencies
- `wwmath.h`, `wwhack.h`, `lookuptable.h`, `stdlib.h`, `wwdebug.h`, `wwprofile.h`
- `LookupTableMgrClass`, `WWMATH_PI`, `WWMATH_FLOAT_MAX`
