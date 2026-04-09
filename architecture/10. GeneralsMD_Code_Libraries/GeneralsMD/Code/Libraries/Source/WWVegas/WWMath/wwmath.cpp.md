# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/wwmath.cpp

## Purpose
Initializes and manages mathematical lookup tables and utilities for the WWMath library.

## Responsibilities
- Initializes trigonometric lookup tables (sin, asin, acos, inverse sin).
- Provides random float generation.
- Manages library module linking.
- Integrates with LookupTableMgrClass for table management.

## Key Types
- None

## Key Functions
### WWMath::Init
- Purpose: Initializes trigonometric lookup tables and LookupTableMgrClass.
- Calls: LookupTableMgrClass::Init, acos, asin, sin

### WWMath::Shutdown
- Purpose: Shuts down the LookupTableMgrClass.
- Calls: LookupTableMgrClass::Shutdown

### WWMath::Random_Float
- Purpose: Generates a random float between 0.0 and 1.0.
- Calls: rand

### Do_Force_Links
- Purpose: Forces linking of specific math modules.
- Calls: FORCE_LINK (macro)

## Globals
- _FastAcosTable (float[ARC_TABLE_SIZE]): Precomputed acos values.
- _FastAsinTable (float[ARC_TABLE_SIZE]): Precomputed asin values.
- _FastSinTable (float[SIN_TABLE_SIZE]): Precomputed sin values.
- _FastInvSinTable (float[SIN_TABLE_SIZE]): Precomputed inverse sin values.

## Dependencies
- wwmath.h, wwhack.h, lookuptable.h, stdlib.h, wwdebug.h, wwprofile.h
- LookupTableMgrClass, WWMATH_PI, WWMATH_FLOAT_MAX, FORCE_LINK macro
