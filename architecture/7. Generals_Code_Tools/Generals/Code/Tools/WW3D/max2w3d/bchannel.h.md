# Generals/Code/Tools/WW3D/max2w3d/bchannel.h

## Purpose
Defines the BitChannelClass for managing bit channels in W3D file export, including compression and storage.

## Responsibilities
- Manages bit channel data for animation frames
- Provides bit manipulation (set/get) and compression
- Handles saving bit channel data to chunks
- Tracks default values and empty state

## Key Types
- **BitChannelClass (Class)**: Manages bit channel data for W3D export
- **LogDataDialogClass (Class)**: External dialog class (forward declaration)

## Key Functions
### BitChannelClass()
- Purpose: Constructor for bit channel initialization
- Calls: None

### Set_Bit()
- Purpose: Sets a bit value for a specific frame
- Calls: None

### Set_Bits()
- Purpose: Sets multiple bit values from a BooleanVectorClass
- Calls: None

### Get_Bit()
- Purpose: Retrieves a bit value for a specific frame
- Calls: None

### Save()
- Purpose: Saves bit channel data to a chunk, with optional compression
- Calls: compute_range(), compress()

### is_default()
- Purpose: Checks if a bit matches the default value
- Calls: None

### compute_range()
- Purpose: Determines the range of non-default data
- Calls: None

### remove_packet()
- Purpose: Removes a packet from the compressed bit channel
- Calls: None

### find_useless_packet()
- Purpose: Finds packets that can be removed during compression
- Calls: None

### compress()
- Purpose: Compresses the bit channel data
- Calls: find_useless_packet(), remove_packet()

## Globals
- None

## Dependencies
- always.h
- bittype.h (BooleanVectorClass)
- chunkio.h (Chunk
