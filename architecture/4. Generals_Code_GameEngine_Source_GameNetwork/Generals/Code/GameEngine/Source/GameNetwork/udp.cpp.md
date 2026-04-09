# Generals/Code/GameEngine/Source/GameNetwork/udp.cpp

## Purpose
Implements a UDP socket wrapper class for cross-platform networking in the game engine.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Handles platform-specific socket APIs (Windows/Unix)
- Provides error reporting and status checking
- Supports non-blocking I/O and buffer size configuration

## Key Types
- UDP (Class): UDP socket wrapper with networking operations
- sockStat (Enum): Socket status/error codes
- AsciiString (Type): String utility for error messages

## Key Functions
### UDP::Bind
- Purpose: Binds the UDP socket to a host and port
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

### UDP::GetStatus
- Purpose: Converts system errors to internal status codes
- Calls: None (uses m_lastError)

## Globals
- None

## Dependencies
- PreRTS.h, GameEngine.h, udp.h
- Winsock2.h (Windows), sys/socket.h (Unix)
- External symbols: socket, bind, sendto, recvfrom, setsockopt, getsockopt, gethostbyname, inet_addr, htonl, htons, ntohl, ntohs
