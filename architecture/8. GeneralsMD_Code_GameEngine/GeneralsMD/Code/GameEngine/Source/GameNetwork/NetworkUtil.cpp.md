# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetworkUtil.cpp

## Purpose
Provides utility functions for network command handling and IP resolution in the game engine.

## Responsibilities
- Resolves hostnames/IP addresses to numeric values
- Generates unique command IDs
- Determines command properties (ACK requirements, synchronization needs)
- Provides debugging utilities for network buffers

## Key Types
- None

## Key Functions
### ResolveIP
- Purpose: Converts hostname or IP string to 32-bit unsigned integer
- Calls: gethostbyname, inet_addr

### GenerateNextCommandID
- Purpose: Generates sequential command IDs starting from 64000
- Calls: None

### DoesCommandRequireACommandID
- Purpose: Checks if a command type requires a unique ID
- Calls: None

### CommandRequiresAck
- Purpose: Determines if a command requires acknowledgment
- Calls: None

### IsCommandSynchronized
- Purpose: Checks if a command type is synchronized
- Calls: None

### CommandRequiresDirectSend
- Purpose: Determines if a command should bypass packet router
- Calls: None

### GetAsciiNetCommandType
- Purpose: Converts command type enum to human-readable string
- Calls: None

## Globals
- MAX_FRAMES_AHEAD (Int): Maximum frames ahead in network synchronization
- MIN_RUNAHEAD (Int): Minimum runahead frames
- FRAME_DATA_LENGTH (Int): Length of frame data buffer
- FRAMES_TO_KEEP (Int): Number of frames to keep in buffer

## Dependencies
- "GameNetwork/NetworkUtil.h"
- "PreRTS.h"
- DEBUG_LOG (macro)
- AsciiString, NetCommandType, NetCommandMsg (external types)
- Standard C library functions (gethostbyname, inet_addr, etc.)
