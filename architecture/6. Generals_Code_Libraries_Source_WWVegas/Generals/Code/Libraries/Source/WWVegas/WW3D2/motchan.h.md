# Generals/Code/Libraries/Source/WWVegas/WW3D2/motchan.h

## Purpose
Defines classes for handling motion channels in 3D animations, including vector and bit channels with various compression schemes.

## Responsibilities
- Define motion channel classes for animation data storage
- Support both raw and compressed animation formats
- Provide methods for retrieving animation data at specific frames
- Manage memory allocation/deallocation for animation data

## Key Types
- **MotionChannelClass (Class)**: Base class for storing motion data (position/orientation) for animation pivots.
- **BitChannelClass (Class)**: Stores boolean "on/off" values per animation frame.
- **TimeCodedMotionChannelClass (Class)**: Compressed motion channel using time-coded packets.
- **AdaptiveDeltaMotionChannelClass (Class)**: Motion channel using adaptive delta compression.
- **TimeCodedBitChannelClass (Class)**: Compressed bit channel using time-coded packets.
- **Quaternion (Class)**: Used for orientation data (referenced but not defined here).

## Key Functions
### MotionChannelClass::Get_Vector
- Purpose: Retrieves animation vector data for a specific frame.
- Calls: set_identity

### BitChannelClass::Get_Bit
- Purpose: Retrieves boolean value for a specific frame.
- Calls: None

### TimeCodedMotionChannelClass::Get_Vector
- Purpose: Retrieves motion data using time-coded compression.
- Calls: get_index, binary_search_index

### AdaptiveDeltaMotionChannelClass::Get_Vector
- Purpose: Retrieves motion data using adaptive delta compression.
- Calls: getframe, decompress

## Globals
- None

## Dependencies
- Key includes: "always.h", "bittype.h", "w3d_file.h", "quat.h"
- External symbols: ChunkLoadClass, Quaternion, W3DMPO (inheritance), ANIM_CHANNEL_Q (enum)
