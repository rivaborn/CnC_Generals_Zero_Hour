# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hcanim.h

## Purpose
Header file defining the `HCompressedAnimClass` for handling compressed animation data in the W3D engine.

## Responsibilities
- Declares the `HCompressedAnimClass` and related structures for compressed animation.
- Provides methods to load, query, and manipulate compressed animation data.
- Manages motion channels (translation, rotation, visibility) for hierarchy nodes.

## Key Types
- `HCompressedAnimClass` (Class): Main class for compressed animation data.
- `NodeCompressedMotionStruct` (Struct): Stores compressed motion data per node.
- `TimeCodedMotionChannelClass` (Class): Time-coded motion channel.
- `TimeCodedBitChannelClass` (Class): Time-coded bit channel (e.g., visibility).
- `AdaptiveDeltaMotionChannelClass` (Class): Adaptive delta motion channel.
- `HTreeClass` (Class): Hierarchy tree (forward declaration).
- `ChunkLoadClass` (Class): Chunk loading utility.
- `ChunkSaveClass` (Class): Chunk saving utility.
- `(anonymous enum)` (Enum): Error codes (`OK`, `LOAD_ERROR`).

## Key Functions
### `HCompressedAnimClass::Load_W3D`
- Purpose: Loads compressed animation data from a W3D file.
- Calls: `read_channel`, `read_bit_channel`, `add_channel`, `add_bit_channel`.

### `HCompressedAnimClass::Get_Translation`
- Purpose: Retrieves translation data for a node at a given frame.
- Calls: None (direct access).

### `HCompressedAnimClass::Get_Orientation`
- Purpose: Retrieves orientation data for a node at a given frame.
- Calls: None (direct access).

### `HCompressedAnimClass::Get
