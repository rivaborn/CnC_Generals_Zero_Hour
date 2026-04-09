# Generals/Code/Libraries/Source/WWVegas/WW3D2/hcanim.cpp

## Purpose
Handles compressed animation data loading, storage, and retrieval for hierarchical models in the W3D engine.

## Responsibilities
- Loads compressed animation data from W3D files
- Manages motion channels (translation, rotation, visibility)
- Provides frame-based animation data retrieval
- Supports two compression flavors (time-coded and adaptive delta)

## Key Types
- **NodeCompressedMotionStruct (Class)**: Stores motion data for a single node (translation, rotation, visibility channels)
- **HCompressedAnimClass (Class)**: Main animation class managing all node motions and animation metadata

## Key Functions
### HCompressedAnimClass::Load_W3D
- Purpose: Loads compressed animation from a W3D file
- Calls: Free(), WW3DAssetManager::Get_Instance()->Get_HTree(), read_channel(), add_channel(), read_bit_channel(), add_bit_channel()

### HCompressedAnimClass::Get_Translation
- Purpose: Retrieves translation vector for a node at a specific frame
- Calls: TimeCodedMotionChannelClass::Get_Vector(), AdaptiveDeltaMotionChannelClass::Get_Vector()

### HCompressedAnimClass::Get_Orientation
- Purpose: Retrieves orientation quaternion for a node at a specific frame
- Calls: TimeCodedMotionChannelClass::Get_QuatVector(), AdaptiveDeltaMotionChannelClass::Get_QuatVector()

### HCompressedAnimClass::Get_Visibility
- Purpose: Checks visibility state for a node at a specific frame
- Calls: TimeCodedBitChannelClass::Get_Bit()

## Globals
- None

## Dependencies
- hcanim.h, assetmgr.h, htree.h, motchan.h, chunkio.h, w3d_file.h, wwdebug.h
- TimeCodedMotionChannelClass, AdaptiveDeltaMotionChannelClass, TimeCodedBitChannelClass, HTreeClass, ChunkLoadClass, Vector3, Quaternion, Matrix3D
