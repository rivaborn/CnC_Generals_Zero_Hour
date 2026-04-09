# Generals/Code/Libraries/Source/WWVegas/WW3D2/prim_anim.h

## Purpose
Defines animation channel classes for primitive animations in the W3D engine, supporting keyframe-based interpolation.

## Responsibilities
- Provides `PrimitiveAnimationChannelClass` template for animated data channels
- Implements `KeyClass` for storing keyframe data
- Defines `LERPAnimationChannelClass` for linear interpolation
- Handles serialization via `ChunkSaveClass`/`ChunkLoadClass`

## Key Types
- `PrimitiveAnimationChannelClass<T>` (Class): Base template for animation channels
- `KeyClass` (Class): Stores keyframe time/value pairs
- `LERPAnimationChannelClass<T>` (Class): Linear interpolation implementation
- `ChunkSaveClass`/`ChunkLoadClass` (Forward declarations): Serialization interfaces

## Key Functions
### `Evaluate(float time)`
- Purpose: Evaluates animation value at given time
- Calls: `m_Data.Count()`, `Get_Time()`, `Get_Value()`

### `Save(ChunkSaveClass &csave)`
- Purpose: Serializes animation data
- Calls: `Begin_Chunk()`, `WRITE_MICRO_CHUNK()`

### `Load(ChunkLoadClass &cload)`
- Purpose: Deserializes animation data
- Calls: `Open_Chunk()`, `Load_Variables()`

## Globals
- `CHUNKID_VARIABLES` (Enum): Chunk ID constant
- `VARID_KEY` (Enum): Micro-chunk ID constant

## Dependencies
- `simplevec.h` (SimpleDynVecClass)
- `chunkio.h` (ChunkSaveClass/ChunkLoadClass)
- `WRITE_MICRO_CHUNK` macro
