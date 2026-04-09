# Generals/Code/Libraries/Source/WWVegas/WW3D2/motchan.cpp

## Purpose
Handles motion channel data structures and decompression for W3D animations, including adaptive delta compression.

## Responsibilities
- Manages motion channel classes (MotionChannelClass, BitChannelClass, TimeCodedMotionChannelClass, AdaptiveDeltaMotionChannelClass)
- Implements loading and decompression of animation data from W3D files
- Provides frame interpolation and quaternion slerping for animations
- Handles memory allocation/deallocation for motion data

## Key Types
- **MotionChannelClass (Class)**: Base class for motion channel data storage
- **BitChannelClass (Class)**: Handles bit-packed animation channels
- **TimeCodedMotionChannelClass (Class)**: Manages time-coded motion data
- **AdaptiveDeltaMotionChannelClass (Class)**: Implements adaptive delta compression/decompression
- **W3dAnimChannelStruct (Struct)**: W3D file format structure for animation channels

## Key Functions
### MotionChannelClass::Load_W3D
- Purpose: Loads motion channel data from a W3D chunk
- Calls: cload.Read

### BitChannelClass::Load_W3D
- Purpose: Reads bit channel data from a W3D chunk
- Calls: cload.Read

### AdaptiveDeltaMotionChannelClass::decompress
- Purpose: Decompresses adaptive delta-encoded motion data
- Calls: None (uses filtertable)

### AdaptiveDeltaMotionChannelClass::getframe
- Purpose: Retrieves decompressed frame data with caching
- Calls: decompress

### AdaptiveDeltaMotionChannelClass::Get_Vector
- Purpose: Interpolates motion data for non-integer frames
- Calls: getframe, WWMath::Lerp

## Globals
- **filtertable (float[256])**: Precomputed filter values for adaptive delta decompression
- **table_valid (bool)**: Flag indicating if filter table is initialized

## Dependencies
- Key includes: "motchan.h", "w3d_file.h", "chunkio.h", "vector.h", "wwmath.h", "quat.h"
- External symbols: MSGW3DNEWARRAY, ChunkLoadClass, W3dAnimChannelStruct, W3dBitChannelStruct, W3dTimeCodedAnimChannelStruct, W3dAdaptiveDeltaAnimChannelStruct, Quaternion, WWMath::Lerp
