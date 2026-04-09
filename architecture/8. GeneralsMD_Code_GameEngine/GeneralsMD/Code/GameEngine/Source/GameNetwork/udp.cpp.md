# GeneralsMD/Code/GameEngine/Source/GameNetwork/udp.cpp

## Purpose
Implements a UDP socket wrapper class for cross-platform networking in the SAGE engine.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Handles platform-specific differences (Windows/Unix)
- Provides error reporting and status checking
- Supports broadcast and buffer size configuration

## Key Types
- UDP (Class): UDP socket wrapper
- sockStat (Enum): Socket status/error codes

## Key Functions
### UDP::Bind
- Purpose: Binds the socket to a specific host/port or IP/port
- Calls: gethostbyname, socket, bind, getsockname, SetBlocking

### UDP::Write
- Purpose: Sends data over UDP to a specified address
- Calls: sendto, ClearStatus

### UDP::Read
- Purpose: Receives data from UDP socket
- Calls: recvfrom, ClearStatus

### UDP::SetBlocking
- Purpose: Configures socket blocking mode
- Calls: ioctlsocket (Windows) or fcntl (Unix)

## Globals
- None

## Dependencies
- PreRTS.h, GameEngine.h, udp.h
- Winsock2.h (Windows), sys/socket.h (Unix)
- AsciiString class
- Platform-specific socket APIs
