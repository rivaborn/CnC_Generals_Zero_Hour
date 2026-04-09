# Generals/Code/Tools/WW3D/max2w3d/vchannel.cpp

## Purpose
Handles vector channel animation data compression and optimization for W3D export.

## Responsibilities
- Manages vector channel data storage and access
- Implements adaptive delta compression for animation data
- Optimizes animation channels by removing redundant keyframes
- Handles quaternion-specific interpolation for rotation data
- Generates filter tables for compression algorithms

## Key Types
- **VectorChannelClass (Class)**: Manages vector animation channels with compression and optimization
- **AdaptiveDeltaPacketStruct (Struct)**: Bit-packed structure for adaptive delta compression packets
- **W3dTimeCodedAnimChannelStruct (External)**: Time-coded animation channel structure

## Key Functions
### `VectorChannelClass::SaveTimeCoded`
- Purpose: Saves time-coded animation channel with compression
- Calls: `compress`, `get_value`, `ExportLog::printf`

### `VectorChannelClass::test_compress`
- Purpose: Tests compression quality for adaptive delta packets
- Calls: None (standalone test function)

### `VectorChannelClass::compress`
- Purpose: Compresses vector data using adaptive delta encoding
- Calls: None (standalone compression function)

### `VectorChannelClass::find_useless_packet`
- Purpose: Identifies redundant keyframes for removal
- Calls: None (standalone optimization function)

### `VectorChannelClass::find_least_useful_packet`
- Purpose: Finds least important keyframe for removal
- Calls: None (standalone optimization function)

## Globals
- **filtertable (float[256])**: Precomputed filter values for compression
- **table_valid (bool)**: Flag indicating if filter table is initialized

## Dependencies
- Key includes: `vchannel.h`, `w3d_file.h`, `w3dquat.h`, `bchannel.h`, `exportlog.h`
- External symbols: `W3dTimeCodedAnimChannelStruct`, `Quaternion`, `Slerp`, `Inverse`, `WWMath::Lerp`
