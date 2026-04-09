# Generals/Code/Tools/matchbot/wnet/udp.h

## Purpose
Defines a cross-platform UDP socket wrapper class for network communication.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Provides error handling via socket status codes
- Supports blocking/non-blocking modes and buffer management
- Handles platform-specific socket APIs (Windows/Unix)

## Key Types
- **UDP (Class)**: Cross-platform UDP socket wrapper
- **sockStat (Enum)**: Socket operation status codes (OK, UNKNOWN, ISCONN, etc.)

## Key Functions
### UDP::Bind
- Purpose: Binds the socket to a specific IP and port
- Calls: Platform-specific socket APIs

### UDP::Write
- Purpose: Sends UDP datagram to specified IP/port
- Calls: Platform-specific sendto()

### UDP::Read
- Purpose: Receives UDP datagram with sender info
- Calls: Platform-specific recvfrom()

### UDP::Wait
- Purpose: Waits for socket activity using select()
- Calls: Platform-specific select()

## Globals
- **DEFAULT_PROTOCOL (const)**: Default protocol value (0)

## Dependencies
- Platform-specific includes (winsock.h, sys/socket.h, etc.)
- WLib types (wstypes.h, wtime.h)
- Standard C libraries (stdio.h, string.h, errno.h)
