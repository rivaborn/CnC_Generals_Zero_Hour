# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tcbspline.h

## Purpose
Defines a 3D TCB (Tension-Continuity-Bias) spline class for smooth interpolation between key points.

## Responsibilities
- Manage 3D spline key points with TCB parameters
- Update tangents based on TCB parameters
- Provide save/load functionality for persistence
- Inherit from HermiteSpline3DClass

## Key Types
- **TCBSpline3DClass (Class)**: Main spline class handling TCB parameters
- **TCBClass (Class)**: Stores tension, continuity, and bias parameters for each key

## Key Functions
### Add_Key
- Purpose: Add a new key point to the spline
- Calls: Not inferable

### Set_TCB_Params
- Purpose: Set TCB parameters for a specific key
- Calls: Not inferable

### Update_Tangents
- Purpose: Recalculate tangents based on current TCB parameters
- Calls: Not inferable

### Save/Load
- Purpose: Persist spline data to/from chunk files
- Calls: Not inferable

## Globals
- None

## Dependencies
- `hermitespline.h` (base class)
- `DynamicVectorClass` (for parameter storage)
- `Vector3` (for 3D points)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (for serialization)
