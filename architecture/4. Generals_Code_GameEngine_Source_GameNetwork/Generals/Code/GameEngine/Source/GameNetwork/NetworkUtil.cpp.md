# Generals/Code/GameEngine/Source/GameNetwork/NetworkUtil.cpp

## Purpose
Provides utility functions for network command handling and IP resolution in the game engine.

## Responsibilities
- Resolve hostnames/IPs to numeric addresses
- Generate and manage network command IDs
- Determine command properties (ACK requirements, synchronization, direct send)
- Convert command types to human-readable strings
- Debug logging for network buffers

## Key Types
- None

## Key Functions
### ResolveIP
- Purpose: Converts a hostname or IP string to a 32-bit unsigned integer
- Calls: `inet_addr`, `gethostbyname`

### GenerateNextCommandID
- Purpose: Generates the next sequential network command ID
- Calls: None

### DoesCommandRequireACommandID
- Purpose: Checks if a command type requires a unique command ID
- Calls: None

### CommandRequiresAck
- Purpose: Determines if a command requires acknowledgment
- Calls: `getNetCommandType`

### IsCommandSynchronized
- Purpose: Checks if a command type is synchronized
- Calls: None

### CommandRequiresDirectSend
- Purpose: Determines if a command requires direct player-to-player sending
- Calls: `getNetCommandType`

### GetAsciiNetCommandType
- Purpose: Converts a NetCommandType enum to its string representation
- Calls: `set`

## Globals
- MAX_FRAMES_AHEAD (Int): Maximum frames ahead in network synchronization
- MIN_RUNAHEAD (Int): Minimum runahead frames
- FRAME_DATA_LENGTH (Int): Length of frame data buffer
- FRAMES_TO_KEEP (Int): Number of frames to keep in buffer

## Dependencies
- `NetworkUtil.h` (header)
- `PreRTS.h` (engine precompiled header)
- `AsciiString`, `NetCommandType`, `NetCommandMsg` (types)
- `inet_addr`, `gethostbyname` (POSIX networking)
- `DEBUG_LOG` (logging macro)
