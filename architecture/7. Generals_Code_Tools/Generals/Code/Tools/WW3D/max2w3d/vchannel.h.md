# Generals/Code/Tools/WW3D/max2w3d/vchannel.h

## Purpose
Defines classes for handling vector-based animation channels, including compression and optimization for W3D file export.

## Responsibilities
- Manages vector data for animation channels (X, Y, Z, orientation)
- Tracks non-zero vector ranges for efficient storage
- Provides compression and optimization for motion data
- Handles identity vector checks and range computation

## Key Types
- **BitChannelClass (Class)**: Not defined here; used for bit-level channel operations.
- **VectorChannelClass (Class)**: Container for vector animation data with compression support.

## Key Functions
### VectorChannelClass/Set_Vector
- Purpose: Sets a vector at a specific frame.
- Calls: None visible.

### VectorChannelClass/Save
- Purpose: Saves the vector channel data to a chunk.
- Calls: `SaveTimeCoded`, `SaveAdaptiveDelta`.

### VectorChannelClass/compress
- Purpose: Compresses animation data using specified filter and scale.
- Calls: None visible.

### VectorChannelClass/find_useless_packet
- Purpose: Identifies packets that can be removed without significant quality loss.
- Calls: None visible.

### VectorChannelClass/SaveTimeCoded
- Purpose: Saves animation data in a time-coded format.
- Calls: None visible.

### VectorChannelClass/SaveAdaptiveDelta
- Purpose: Saves animation data using adaptive delta compression.
- Calls: None visible.

## Globals
- **DEFAULT_LOSSY_ERROR_TOLERANCE (float32)**: Default tolerance for lossy compression.
- **PACKETS_ALL_USEFUL (uint32)**: Flag indicating all packets are useful.

## Dependencies
- `always.h`, `bittype.h`, `chunkio.h`, `w3d_file.h`
- `
