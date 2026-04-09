# GeneralsMD/Code/GameEngine/Include/Common/QuickTrig.h

## Purpose
Provides fast, approximate trigonometric functions and magnitude estimation for game performance optimization.

## Responsibilities
- Implements fast magnitude estimation without square root
- Provides table-based sine, cosine, tangent, and their reciprocals
- Handles angle normalization and sign preservation
- Uses precomputed lookup tables for efficiency

## Key Types
None

## Key Functions
### QMag
- Purpose: Estimates magnitude of 3D vector without square root
- Calls: fabs

### QSin
- Purpose: Computes sine using lookup table with angle normalization
- Calls: None

### QCos
- Purpose: Computes cosine by transforming angle and calling QSin
- Calls: QSin

### QTan
- Purpose: Computes tangent using tangent lookup table
- Calls: None

### QCsc
- Purpose: Computes cosecant as reciprocal of sine
- Calls: QSin

### QSec
- Purpose: Computes secant as reciprocal of cosine
- Calls: QCos

### QCot
- Purpose: Computes cotangent as reciprocal of tangent
- Calls: QTan

## Globals
- TheQuickSinTable (Real[]): Precomputed sine values
- TheQuickTanTable (Real[]): Precomputed tangent values
- TheQuickSinTableCount (Real): Size of sine table
- TheQuickTanTableCount (Real): Size of tangent table

## Dependencies
- Uses Real type (floating-point)
- Uses PI constant
- Uses fabs function
- Uses REAL_TO_INT macro (not shown)
