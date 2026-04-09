# Generals/Code/Libraries/Source/WWVegas/WWMath/cardinalspline.h

## Purpose
Defines 1D and 3D cardinal spline classes for interpolation, extending Hermite splines with tightness control.

## Responsibilities
- Manage key points and tangents for spline interpolation
- Provide tightness adjustment per key
- Support serialization via Save/Load
- Maintain dynamic tightness values

## Key Types
- **CardinalSpline3DClass (Class)**: 3D cardinal spline with tightness control
- **CardinalSpline1DClass (Class)**: 1D cardinal spline with tightness control

## Key Functions
### Add_Key
- Purpose: Adds a key point to the spline
- Calls: Not inferable

### Update_Tangents
- Purpose: Recalculates tangents based on current keys and tightness
- Calls: Not inferable

### Save/Load
- Purpose: Serialization support for spline data
- Calls: ChunkSaveClass/ChunkLoadClass methods

## Globals
- None

## Dependencies
- `hermitespline.h` (base class)
- `DynamicVectorClass<float>` (for tightness storage)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (serialization)
- `Vector3` (for 3D points)
