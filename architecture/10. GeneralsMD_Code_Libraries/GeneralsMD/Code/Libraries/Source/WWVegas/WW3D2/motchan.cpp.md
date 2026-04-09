# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/motchan.cpp

## Purpose
Handles motion channel data loading, compression, and decompression for W3D animations.

## Responsibilities
- Loads motion channels from W3D files
- Manages compressed and uncompressed motion data
- Provides frame interpolation for animations
- Handles adaptive delta compression/decompression
- Manages bit channels for animation data

## Key Types
- **MotionChannelClass**: Base class for motion channel data (position/rotation)
- **BitChannelClass**: Handles bit-packed animation channels
- **TimeCodedMotionChannelClass**: Time-coded motion channel variant
- **AdaptiveDeltaMotionChannelClass**: Adaptive delta compression/decompression
- **W3dAnimChannelStruct**: W3D file format structure for animation channels

## Key Functions
### MotionChannelClass::Load_W3D
- Purpose: Loads motion channel data from W3D chunk
- Calls: `Do_Data_Compression`

### BitChannelClass::Load_W3D
- Purpose: Loads bit channel data from W3D chunk
- Calls: None

### AdaptiveDeltaMotionChannelClass::decompress
- Purpose: Decompresses adaptive delta-encoded motion data
- Calls: None

### AdaptiveDeltaMotionChannelClass::getframe
- Purpose: Retrieves decompressed frame data with caching
- Calls: `decompress`

### AdaptiveDeltaMotionChannelClass::Get_Vector
- Purpose: Interpolates motion vector between frames
- Calls: `getframe`

### AdaptiveDeltaMotionChannelClass::Get_QuatVector
- Purpose: Interpolates quaternion between frames using slerp
- Calls: `getframe`, `Fast_Slerp`

## Globals
- **filtertable (float[256])**: Precomputed filter values for adaptive delta decompression
- **table_valid (bool)**: Flag indicating if filter table is valid

## Dependencies
- `motchan.h`, `w3d_file.h`, `chunkio.h`, `vector.h`, `quat.h`, `wwmath.h`
- `MSGW3DNEWARRAY`, `WWMath::Lerp`, `Fast_Slerp`, `WWASSERT`
