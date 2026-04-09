# Generals/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.h

## Purpose
Defines classes for handling raw animation data in the W3D engine, including motion channels and node motions.

## Responsibilities
- Define `NodeMotionStruct` for storing motion channels per node.
- Implement `HRawAnimClass` for loading and managing hierarchical animations.
- Provide accessors for animation properties (frames, rate, transforms).
- Support querying motion channel presence and visibility.

## Key Types
- `MotionChannelClass` (Class): Base class for motion channels (not defined here).
- `BitChannelClass` (Class): Base class for bit channels (not defined here).
- `NodeMotionStruct` (Struct): Holds motion channels (translation, rotation, visibility) for a node.
- `HRawAnimClass` (Class): Manages raw animation data for a hierarchy tree.
- `(anonymous enum)` (Enum): Defines status codes (`OK`, `LOAD_ERROR`).

## Key Functions
### `HRawAnimClass::Load_W3D`
- Purpose: Loads animation data from a W3D chunk.
- Calls: `read_channel`, `add_channel`, `read_bit_channel`, `add_bit_channel`.

### `HRawAnimClass::Get_Translation`
- Purpose: Retrieves translation at a specific frame for a node.
- Calls: Not inferable.

### `HRawAnimClass::Get_Orientation`
- Purpose: Retrieves orientation at a specific frame for a node.
- Calls: Not inferable.

### `HRawAnimClass::Get_Transform`
- Purpose: Retrieves full transform (translation + orientation) at a specific frame.
- Calls: Not inferable.

### `HRawAnimClass::Get_Visibility`
- Purpose: Checks visibility at a specific frame for a node.
- Calls: Not inferable.

### `HR
