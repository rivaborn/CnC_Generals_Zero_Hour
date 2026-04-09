# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/prim_anim.h

## Purpose
Defines animation channel classes for primitive 3D objects in the SAGE engine, supporting keyframe-based animation and linear interpolation.

## Responsibilities
- Provides `PrimitiveAnimationChannelClass` template for animated data channels
- Implements `KeyClass` for storing keyframe data
- Defines `LERPAnimationChannelClass` for linear interpolation between keyframes
- Handles serialization via `ChunkSaveClass`/`ChunkLoadClass`
- Manages keyframe operations (add, insert, delete, evaluate)

## Key Types
- **PrimitiveAnimationChannelClass (Class)**: Base template class for animated channels
- **KeyClass (Class)**: Stores keyframe time and value pairs
- **LERPAnimationChannelClass (Class)**: Linear interpolation implementation of animation channel
- **ChunkSaveClass (Class)**: Forward declaration for serialization
- **ChunkLoadClass (Class)**: Forward declaration for deserialization

## Key Functions
### `Evaluate`
- Purpose: Evaluates animation value at given time
- Calls: `Get_Time`, `Get_Value`, `Count`

### `Save`
- Purpose: Serializes animation channel data
- Calls: `Begin_Chunk`, `End_Chunk`, `WRITE_MICRO_CHUNK`

### `Load`
- Purpose: Deserializes animation channel data
- Calls: `Open_Chunk`, `Close_Chunk`, `Load_Variables`

### `Load_Variables`
- Purpose: Handles microchunk loading for keyframes
- Calls: `Open_Micro_Chunk`, `Close_Micro_Chunk`, `Read`

## Globals
- **CHUNKID_VARIABLES (Enum)**: Chunk ID for animation data (0x03150809)
- **VARID_KEY (Enum)**: Microchunk ID for keyframes (1)

## Dependencies
- `simplevec.h` (for `SimpleDynVecClass`)
- `chunkio.h` (for `ChunkSaveClass`/`ChunkLoadClass`)
- `WRITE_MICRO_CHUNK` macro (serialization helper)
