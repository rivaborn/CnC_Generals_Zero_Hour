# Generals/Code/Libraries/Source/WWVegas/WW3D2/snapPts.h

## Purpose
Header file defining the SnapPointsClass for managing 3D snap points in the W3D engine.

## Responsibilities
- Declares SnapPointsClass for storing Vector3 snap points
- Provides W3D loading functionality
- Inherits from DynamicVectorClass and RefCountClass
- Defines ChunkLoadClass dependency

## Key Types
- **SnapPointsClass (Class)**: Manages a collection of 3D snap points with reference counting
- **ChunkLoadClass (Class)**: Forward declaration for W3D chunk loading

## Key Functions
### SnapPointsClass::Load_W3D
- Purpose: Loads snap points from a W3D chunk
- Calls: ChunkLoadClass methods (not specified in header)

## Globals
- None

## Dependencies
- "refcount.h" (RefCountClass)
- "vector.h" (DynamicVectorClass)
- "vector3.h" (Vector3)
- "w3derr.h" (WW3DErrorType)
