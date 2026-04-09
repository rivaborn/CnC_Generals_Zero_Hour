# Generals/Code/Libraries/Source/WWVegas/WWMath/hermitespline.cpp

## Purpose
Implements Hermite spline interpolation for 3D and 1D curves, including persistence and tangent management.

## Responsibilities
- Provides 3D and 1D Hermite spline evaluation
- Manages key points and tangents
- Handles persistence (save/load) for splines
- Computes derivatives of splines
- Supports looping and non-looping curves

## Key Types
- (anonymous enum) (Enum): Chunk IDs for persistence
- HERMITE3D_CHUNK_CURVE3D (Enum): Chunk ID for 3D curve data
- HERMITE3D_CHUNK_TANGENTS (Enum): Chunk ID for 3D tangents
- HERMITE1D_CHUNK_CURVE1D (Enum): Chunk ID for 1D curve data
- HERMITE1D_CHUNK_TANGENTS (Enum): Chunk ID for 1D tangents

## Key Functions
### HermiteSpline3DClass::Evaluate
- Purpose: Evaluates the 3D Hermite spline at a given time
- Calls: Update_Tangents, Find_Interval

### HermiteSpline3DClass::Evaluate_Derivative
- Purpose: Computes the derivative of the 3D Hermite spline at a given time
- Calls: Update_Tangents, Find_Interval

### HermiteSpline1DClass::Evaluate
- Purpose: Evaluates the 1D Hermite spline at a given time
- Calls: Update_Tangents, Find_Interval

## Globals
- _HermiteSpline3DFactory (SimplePersistFactoryClass): Persistence factory for 3D splines
- _HermiteSpline1DFactory (SimplePersistFactoryClass): Persistence factory for 1D splines

## Dependencies
- hermitespline.h
- wwmathids.h
- persistfactory.h
- wwhack.h
