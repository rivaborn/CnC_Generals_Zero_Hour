# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hcanim.cpp

## Purpose
Manages compressed hierarchical animations for 3D models, including loading, processing, and retrieving motion data.

## Responsibilities
- Loads and parses compressed animation data from W3D files
- Stores and manages motion channels (translation, rotation, visibility) per node
- Provides access to animation data (position, orientation, visibility) at specific frames
- Handles different animation compression flavors (time-coded, adaptive delta)

## Key Types
- **NodeCompressedMotionStruct (Class)**: Stores motion data (translation, rotation, visibility) for a single node in the hierarchy
- **HCompressedAnimClass (Class)**: Main animation class that manages all nodes and their motion data
- **ANIM_FLAVOR_TIMECODED / ANIM_FLAVOR_ADAPTIVE_DELTA (Enums)**: Animation compression types

## Key Functions
### HCompressedAnimClass::Load_W3D
- Purpose: Loads compressed animation data from a W3D file
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
