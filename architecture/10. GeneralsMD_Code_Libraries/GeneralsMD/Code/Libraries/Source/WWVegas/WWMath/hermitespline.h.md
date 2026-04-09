# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/hermitespline.h

## Purpose
Defines Hermite spline interpolation classes for 1D and 3D curves, supporting tangent control and key management.

## Responsibilities
- Implement Hermite spline evaluation for 1D and 3D curves
- Manage key points and tangents
- Provide save/load persistence
- Support looping behavior

## Key Types
- **HermiteSpline3DClass (Class)**: 3D Hermite spline interpolation with tangent control
- **TangentsClass (Class)**: Stores in/out tangents for 3D spline
- **HermiteSpline1DClass (Class)**: 1D Hermite spline interpolation with tangent control
- **TangentsClass (Class)**: Stores in/out tangents for 1D spline

## Key Functions
### HermiteSpline3DClass::Evaluate
- Purpose: Evaluates the 3D spline at a given time
- Calls: Not inferable

### HermiteSpline3DClass::Set_Tangents
- Purpose: Sets tangents for a specific key
- Calls: Not inferable

### HermiteSpline1DClass::Evaluate
- Purpose: Evaluates the 1D spline at a given time
- Calls: Not inferable

### HermiteSpline1DClass::Set_Tangents
- Purpose: Sets tangents for a specific key
- Calls: Not inferable

## Globals
- None

## Dependencies
- `curve.h` (base classes Curve3DClass, Curve1DClass)
- `DynamicVectorClass` (for tangent storage)
- `Vector3` (3D math)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass`
