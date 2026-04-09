# Generals/Code/Libraries/Source/WWVegas/WWMath/tcbspline.h

## Purpose
Defines a 3D TCB (Tension-Continuity-Bias) spline class for interpolation, extending Hermite splines.

## Responsibilities
- Manage key points and their TCB parameters (tension, continuity, bias).
- Update tangents based on TCB parameters.
- Provide save/load functionality for persistence.

## Key Types
- **TCBSpline3DClass (Class)**: 3D TCB spline implementation.
- **TCBClass (Class)**: Stores TCB parameters (tension, continuity, bias) for a key.

## Key Functions
### `Add_Key`
- Purpose: Adds a key point with a given time.
- Calls: Not inferable.

### `Set_TCB_Params`
- Purpose: Sets TCB parameters for a specific key.
- Calls: Not inferable.

### `Update_Tangents`
- Purpose: Recalculates tangents based on current TCB parameters.
- Calls: Not inferable.

### `Save` / `Load`
- Purpose: Serializes/deserializes the spline data.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `hermitespline.h` (base class).
- `DynamicVectorClass` (container for TCB parameters).
- `Vector3` (3D point representation).
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (save/load infrastructure).
