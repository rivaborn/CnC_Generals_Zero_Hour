# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/wwmathids.h

## Purpose
Defines chunk IDs for WWMath serialization, used in save/load operations.

## Responsibilities
- Declares enum values for 1D and 3D curve/spline types
- Provides unique identifiers for math objects in save files
- Ensures proper chunk ID allocation via `CHUNKID_WWMATH_BEGIN`

## Key Types
- (anonymous enum) (Enum): Contains all WWMath chunk IDs for serialization

## Key Functions
None.

## Globals
None.

## Dependencies
- `saveloadids.h`: For `CHUNKID_WWMATH_BEGIN` and related constants
