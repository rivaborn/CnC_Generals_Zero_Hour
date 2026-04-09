# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.cpp

## Purpose
Handles loading and processing of hierarchical animation data for the W3D engine.

## Responsibilities
- Loads animation data from files using chunk-based I/O
- Manages motion channels (translation, rotation, visibility) for animated nodes
- Interpolates animation data between frames
- Provides access to animation state (position, orientation, visibility)

## Key Types
- `NodeMotionStruct` (struct): Container for motion channels (X/Y/Z translation, X/Y/Z rotation, quaternion, visibility) for a single node
- `HRawAnimClass` (class): Main animation class that manages all node motions and animation data
- `MotionChannelClass` (class): Base class for animation channels (referenced but not defined here)
- `BitChannelClass` (class): Base class for bit-based animation channels (referenced but not defined here)

## Key Functions
### `HRawAnimClass::Load_W3D`
- Purpose: Loads animation data from a chunked file
- Calls: `Free`, `cload.Open_Chunk`, `cload.Read`, `cload.Close_Chunk`, `read_channel`, `add_channel`, `read_bit_channel`, `add_bit_channel`

### `HRawAnimClass::Get_Translation`
- Purpose: Retrieves interpolated translation vector for a node at a specific frame
- Calls: `WWMath::Float_To_Long`, `Vector3::Lerp`

### `HRawAnimClass::Get_Orientation`
- Purpose: Retrieves interpolated quaternion orientation for a node at a specific frame
- Calls: `WWMath::Float_To_Long`, `Fast_Slerp`

### `HRawAnimClass::Get_Transform`
- Purpose: Retrieves full transform matrix (rotation + translation) for a node at a specific frame
- Calls: `WWMath::Float_To_Long`, `Build_Matrix3D`, `Fast_Slerp`, `Vector3::Lerp`

### `HRawAnimClass::Get_Visibility`
- Purpose: Retrieves visibility state for a node at a specific frame
- Calls: None

## Globals
None

## Dependencies
- `hrawanim.h`, `motchan.h`, `chunkio.h`, `assetmgr.h`, `htree.h`
- `Vector3`, `Quaternion`, `Matrix3D`, `WWMath`, `W3DNEW`, `W3DNEWARRAY`
- `W3D_CHUNK_ANIMATION_HEADER`, `W3D_CHUNK_ANIMATION_CHANNEL`, `W3D_CHUNK_BIT_CHANNEL`
- `ANIM_CHANNEL_X/Y/Z`, `ANIM_CHANNEL_XR/YR/ZR`, `ANIM_CHANNEL_Q`, `BIT_CHANNEL_VIS`
