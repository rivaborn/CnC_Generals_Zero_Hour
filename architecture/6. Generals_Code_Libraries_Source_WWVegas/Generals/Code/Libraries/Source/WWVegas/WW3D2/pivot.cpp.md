# Generals/Code/Libraries/Source/WWVegas/WW3D2/pivot.cpp

## Purpose
Manages pivot points for 3D transformations, including matrix operations and state tracking.

## Responsibilities
- Constructs and initializes pivot objects
- Computes transformation matrices
- Handles matrix capture and update logic
- Manages visibility and world-space translation flags

## Key Types
- **PivotClass (Class)**: Represents a pivot point with transformation matrices and state flags
- **Matrix3D (Type)**: Used for 3D transformation matrices (external)

## Key Functions
### PivotClass::PivotClass
- Purpose: Default constructor initializing member variables
- Calls: None

### PivotClass::PivotClass (copy)
- Purpose: Copy constructor for PivotClass
- Calls: memcpy, MSGW3DNEW (conditional)

### operator=
- Purpose: Assignment operator for PivotClass
- Calls: memcpy, MSGW3DNEW (conditional)

### Capture_Update
- Purpose: Updates the pivot's transform matrix based on captured state
- Calls: Matrix3D::Multiply (conditional), Transform.postMul (conditional), Transform.Adjust_Translation

## Globals
- None

## Dependencies
- pivot.h (header)
- wwmath.h (Matrix3D operations)
- string.h (memcpy)
