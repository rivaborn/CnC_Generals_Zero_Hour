# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/cardinalspline.h

## Purpose
Defines 1D and 3D cardinal spline classes for interpolation with adjustable tightness.

## Responsibilities
- Manage key points and tangents for spline interpolation
- Support tightness adjustment per key
- Provide save/load functionality for persistence
- Inherit from Hermite spline base classes

## Key Types
- **CardinalSpline3DClass (Class)**: 3D cardinal spline with tightness control
- **CardinalSpline1DClass (Class)**: 1D cardinal spline with tightness control

## Key Functions
### Add_Key
- Purpose: Add a new key point to the spline
- Calls: Not inferable

### Update_Tangents
- Purpose: Recalculate tangents based on current keys and tightness
- Calls: Not inferable

### Save/Load
- Purpose: Serialize spline data for persistence
- Calls: ChunkSaveClass/ChunkLoadClass methods

## Globals
- None

## Dependencies
- `hermitespline.h` (base class)
- `DynamicVectorClass` (for tightness storage)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (save/load)
- `Vector3` (for 3D points)
