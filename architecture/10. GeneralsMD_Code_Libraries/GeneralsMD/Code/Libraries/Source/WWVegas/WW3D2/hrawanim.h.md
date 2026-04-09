# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.h

## Purpose
Defines classes for handling raw animation data in the W3D format, including motion channels and node motions.

## Responsibilities
- Define `HRawAnimClass` for storing motion data applied to hierarchy trees.
- Manage motion channels (`MotionChannelClass`) and bit channels (`BitChannelClass`).
- Provide accessors for animation properties (frames, rate, transforms, visibility).
- Handle loading and parsing of W3D animation chunks.

## Key Types
- **MotionChannelClass (Class)**: Represents a motion channel (e.g., translation/rotation).
- **BitChannelClass (Class)**: Represents a bit channel (e.g., visibility flags).
- **NodeMotionStruct (Struct)**: Holds motion channels for a node (X/Y/Z translation, rotation, visibility).
- **HRawAnimClass (Class)**: Main class for raw animation data with frame/transform access.
- **(anonymous enum) (Enum)**: Defines status codes (`OK`, `LOAD_ERROR`).

## Key Functions
### `Load_W3D`
- Purpose: Loads animation data from a W3D chunk.
- Calls: `read_channel`, `add_channel`, `read_bit_channel`, `add_bit_channel`.

### `Get_Translation`
- Purpose: Retrieves translation at a given frame for a pivot.
- Calls: None (direct access).

### `Get_Orientation`
- Purpose: Retrieves orientation at a given frame for a pivot.
- Calls: None (direct access).

### `Get_Transform`
- Purpose: Retrieves full transform matrix at a given frame for a pivot.
- Calls: None (direct access).

### `Is_Node_Motion_Present`
- Purpose: Checks if motion data exists for a node.
- Calls: None (direct access).

### `read_channel
