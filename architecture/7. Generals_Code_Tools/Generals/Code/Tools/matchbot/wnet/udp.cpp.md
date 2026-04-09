# Generals/Code/Tools/matchbot/wnet/udp.cpp

## Purpose
Implements a cross-platform UDP socket wrapper for the matchbot tool.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Provides platform-specific error handling and status reporting
- Supports non-blocking I/O and socket buffer tuning
- Handles both IPv4 addresses and hostnames

## Key Types
- UDP (Class): UDP socket wrapper
- sockStat (Enum): Socket error status codes

## Key Functions
### UDP::Bind(char *Host, uint16 port)
- Purpose: Binds UDP socket to a hostname and port
- Calls: Bind(uint32 IP, uint16 Port), gethostbyname(), inet_addr()

### UDP::Write(uint8 *msg, uint32 len, uint32 IP, uint16 port)
- Purpose: Sends UDP datagram to specified address
- Calls: sendto(), ClearStatus()

### UDP::Read(uint8 *msg, uint32 len, sockaddr_in *from)
- Purpose: Receives UDP datagram with optional sender address
- Calls: recvfrom()

### UDP::Wait(sint32 sec, sint32 usec, fd_set &returnSet)
- Purpose: Waits for socket activity with timeout
- Calls: select(), FD_ZERO(), FD_SET()

## Globals
- None

## Dependencies
- Key includes: "udp.h", "wlib/wdebug.h"
- External symbols: socket(), bind(), sendto(), recvfrom(), select(), gethostbyname(), inet_addr(), setsockopt(), getsockopt(), fcntl(), ioctlsocket(), WSAGetLastError(), errno
- Platform-specific: Windows Sockets API vs POSIX sockets
