# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/snapPts.h

## Purpose
Defines the `SnapPointsClass` for managing 3D snap points in the W3D engine.

## Responsibilities
- Manages a dynamic vector of 3D vectors (snap points)
- Provides W3D chunk loading functionality
- Implements reference counting via `RefCountClass`

## Key Types
- **SnapPointsClass (Class)**: Manages a collection of 3D snap points with reference counting.
- **ChunkLoadClass (Class)**: External class used for chunk loading (not defined here).

## Key Functions
### SnapPointsClass::Load_W3D
- Purpose: Loads snap points from a W3D chunk.
- Calls: `ChunkLoadClass` methods (not specified in header).

## Globals
- None

## Dependencies
- `refcount.h` (for `RefCountClass`)
- `vector.h` (for `DynamicVectorClass`)
- `vector3.h` (for `Vector3`)
- `w3derr.h` (for `WW3DErrorType`)
- `ChunkLoadClass` (external)
