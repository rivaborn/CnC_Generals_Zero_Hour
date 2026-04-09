# Generals/Code/Tools/WW3D/max2w3d/bchannel.cpp

## Purpose
Manages bit channels for animation data in the W3D format, supporting compression and serialization.

## Responsibilities
- Stores and manipulates boolean animation data per frame
- Compresses bit channel data using time-coded optimization
- Serializes bit channel data to W3D file chunks
- Tracks non-default bit ranges for efficient storage

## Key Types
- **BitChannelClass (Class)**: Manages a boolean animation channel with compression support
- **W3dBitChannelStruct (Struct)**: Raw bit channel data structure
- **W3dTimeCodedBitChannelStruct (Struct)**: Time-coded compressed bit channel format

## Key Functions
### `Set_Bit(int frameidx, bool bit)`
- Purpose: Sets a bit value at a specific frame index
- Calls: None

### `Save(ChunkSaveClass & csave, bool compress)`
- Purpose: Serializes the bit channel to a W3D chunk, optionally compressing
- Calls: `Begin_Chunk`, `Write`, `End_Chunk`, `compute_range`, `compress`, `Set_Bit`

### `compress(W3dTimeCodedBitChannelStruct * c)`
- Purpose: Compresses time-coded bit channel by removing redundant packets
- Calls: `find_useless_packet`, `remove_packet`

### `find_useless_packet(W3dTimeCodedBitChannelStruct * c)`
- Purpose: Identifies packets that can be removed during compression
- Calls: None

### `remove_packet(W3dTimeCodedBitChannelStruct * c, uint32 packet_idx)`
- Purpose: Removes a packet from the time-coded bit channel
- Calls: None

## Globals
- **PACKETS_ALL_USEFUL (const)**: Flag indicating all packets are necessary (0xFFFFFFFF)

## Dependencies
- `bchannel.h`, `w3d_file.h`, `logdlg.h`, `exportlog.h`
- `ChunkSaveClass`, `BooleanVectorClass`, `W3dBitChannelStruct`, `W3dTimeCodedBitChannelStruct`
