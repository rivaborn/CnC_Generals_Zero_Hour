# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/motchan.h

## Purpose
Defines motion channel classes for animation data handling in the W3D engine.

## Responsibilities
- Declares classes for motion, bit, and time-coded animation channels
- Provides interfaces for loading W3D animation data
- Manages vector and quaternion data for skeletal animations
- Handles compressed and adaptive delta motion channels

## Key Types
- **MotionChannelClass (Class)**: Base class for motion channels (X/Y/Z/quaternion)
- **BitChannelClass (Class)**: Stores boolean "on/off" values per animation frame
- **TimeCodedMotionChannelClass (Class)**: Time-coded motion channel for efficient storage
- **AdaptiveDeltaMotionChannelClass (Class)**: Adaptive delta-compressed motion channel
- **TimeCodedBitChannelClass (Class)**: Time-coded boolean channel
- **Quaternion (Class)**: Used for orientation data (forward declaration)

## Key Functions
### `MotionChannelClass::Get_Vector`
- Purpose: Retrieves vector data for a specific frame
- Calls: `set_identity`

### `BitChannelClass::Get_Bit`
- Purpose: Retrieves boolean value for a specific frame
- Calls: None

### `TimeCodedMotionChannelClass::Get_Vector`
- Purpose: Retrieves time-coded vector data
- Calls: `get_index`, `binary_search_index`

### `AdaptiveDeltaMotionChannelClass::Get_Vector`
- Purpose: Retrieves adaptive delta-compressed vector data
- Calls: `decompress`

## Globals
- None

## Dependencies
- `always.h`, `bittype.h`, `w3d_file.h`, `quat.h`
- `ChunkLoadClass`, `Quaternion` (forward declarations)
- `W3DMPO` base class
- `ANIM_CHANNEL_Q` constant
