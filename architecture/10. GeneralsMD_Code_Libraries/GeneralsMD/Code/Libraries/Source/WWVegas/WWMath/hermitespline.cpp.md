# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/hermitespline.cpp

## Purpose
Implements Hermite spline interpolation for 3D and 1D curves, including persistence and tangent management.

## Responsibilities
- Provides 3D and 1D Hermite spline evaluation
- Manages key points and tangents
- Handles persistence (save/load) for splines
- Computes derivatives for spline curves
- Supports looping and non-looping splines

## Key Types
- (anonymous enum) (Enum): Chunk IDs for persistence
- HERMITE3D_CHUNK_CURVE3D (Enum): 3D curve chunk ID
- HERMITE3D_CHUNK_TANGENTS (Enum): 3D tangents chunk ID
- HERMITE1D_CHUNK_CURVE1D (Enum): 1D curve chunk ID
- HERMITE1D_CHUNK_TANGENTS (Enum): 1D tangents chunk ID

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
- _HermiteSpline3DFactory (SimplePersistFactoryClass): Factory for 3D Hermite splines
- _HermiteSpline1DFactory (SimplePersistFactoryClass): Factory for 1D Hermite splines

## Dependencies
- hermitespline.h
- wwmathids.h
- persistfactory.h
- wwhack.h
- Vector3, Curve3DClass, Curve1DClass, ChunkSaveClass, ChunkLoadClass, PersistFactoryClass
