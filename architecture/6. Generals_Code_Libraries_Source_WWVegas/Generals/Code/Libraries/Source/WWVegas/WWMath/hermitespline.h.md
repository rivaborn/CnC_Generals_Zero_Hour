# Generals/Code/Libraries/Source/WWVegas/WWMath/hermitespline.h

## Purpose
Defines Hermite spline interpolation classes for 1D and 3D curves, supporting tangent control and keyframe manipulation.

## Responsibilities
- Provides 3D and 1D Hermite spline implementations
- Manages key points and tangents for interpolation
- Supports looping and derivative evaluation
- Implements persistence (save/load) for splines

## Key Types
- **HermiteSpline3DClass (Class)**: 3D Hermite spline with tangent control
- **TangentsClass (Class)**: Stores in/out tangents for 3D spline
- **HermiteSpline1DClass (Class)**: 1D Hermite spline with tangent control
- **TangentsClass (Class)**: Stores in/out tangents for 1D spline

## Key Functions
### HermiteSpline3DClass::Evaluate
- Purpose: Evaluates the spline at a given time
- Calls: Not inferable

### HermiteSpline3DClass::Set_Tangents
- Purpose: Sets tangents for a specific key
- Calls: Not inferable

### HermiteSpline1DClass::Evaluate
- Purpose: Evaluates the 1D spline at a given time
- Calls: Not inferable

## Globals
- None

## Dependencies
- `curve.h` (base classes Curve3DClass, Curve1DClass)
- `DynamicVectorClass` (for tangent storage)
- `Vector3` (3D math)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (persistence)
