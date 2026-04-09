# GeneralsMD/Code/GameEngine/Source/Common/System/QuickTrig.cpp

## Purpose
Provides fast trigonometric function approximations using precomputed lookup tables.

## Responsibilities
- Defines sine and tangent lookup tables
- Calculates table sizes
- Exposes tables for external use

## Key Types
None

## Key Functions
None

## Globals
- TheQuickSinTable (Real[]): Precomputed sine values for angles 0 to 90 degrees
- TheQuickTanTable (Real[]): Precomputed tangent values for angles 0 to 90 degrees
- TheQuickSinTableCount (Real): Number of entries in sine table
- TheQuickTanTableCount (Real): Number of entries in tangent table

## Dependencies
- "PreRTS.h" (include)
- "Common/QuickTrig.h" (include)
- Real type (external)
