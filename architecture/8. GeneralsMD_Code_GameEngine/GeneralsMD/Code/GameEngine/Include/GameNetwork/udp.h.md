# GeneralsMD/Code/GameEngine/Include/GameNetwork/udp.h

## Purpose
Defines a cross-platform UDP socket wrapper class for network communication.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Provides error handling via `sockStat` enum
- Supports platform-specific socket APIs (Windows/Unix)
- Configures socket buffers and broadcast permissions

## Key Types
- **UDP (Class)**: Cross-platform UDP socket wrapper
- **sockStat (Enum)**: Socket operation status codes (OK, UNKNOWN, ISCONN, etc.)

## Key Functions
### UDP::Bind
- Purpose: Binds the socket to a local IP/port
- Calls: Platform-specific socket APIs

### UDP::Write
- Purpose: Sends UDP datagram to specified IP/port
- Calls: Platform-specific sendto()

### UDP::Read
- Purpose: Receives UDP datagram with sender info
- Calls: Platform-specific recvfrom()

### UDP::SetBlocking
- Purpose: Configures socket blocking mode
- Calls: Platform-specific fcntl/ioctlsocket()

## Globals
- **DEFAULT_PROTOCOL (const)**: Default protocol value (0)

## Dependencies
- Platform-specific headers (winsock.h, sys/socket.h, etc.)
- `BaseType.h` for Int/UnsignedInt types
- `sockaddr_in` from system headers
