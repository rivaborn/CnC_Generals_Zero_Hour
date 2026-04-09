# Generals/Code/Libraries/Source/WWVegas/WW3D2/hcanim.h

## Purpose
Defines the `HCompressedAnimClass` for handling compressed animation data in the W3D engine.

## Responsibilities
- Load and manage compressed animation data
- Provide access to animation properties (frames, rate, transforms)
- Support motion channel and bit channel operations
- Interface with hierarchy tree nodes for animation application

## Key Types
- `HCompressedAnimClass` (Class): Main compressed animation handler
- `NodeCompressedMotionStruct` (Struct): Stores node motion data
- `TimeCodedMotionChannelClass` (Class): Time-coded motion channel
- `AdaptiveDeltaMotionChannelClass` (Class): Adaptive delta motion channel
- `TimeCodedBitChannelClass` (Class): Time-coded bit channel
- `HTreeClass` (Class): Hierarchy tree reference
- `ChunkLoadClass`/`ChunkSaveClass` (Classes): File I/O helpers
- `(anonymous enum)` (Enum): Status codes (OK, LOAD_ERROR)

## Key Functions
### `Load_W3D`
- Purpose: Load animation data from a W3D file
- Calls: `read_channel`, `read_bit_channel`, `add_channel`, `add_bit_channel`

### `Get_Translation`/`Get_Orientation`/`Get_Transform`
- Purpose: Retrieve animation transforms for a node at a given frame
- Calls: None (direct computation)

### `Is_Node_Motion_Present`
- Purpose: Check if motion data exists for a node
- Calls: None

### `Has_X_Translation`/`Has_Y_Translation`/`Has_Z_Translation`/`Has_Rotation`/`Has_Visibility`
- Purpose: Check presence of specific motion channels
- Calls: None

### `Free`
- Purpose:
