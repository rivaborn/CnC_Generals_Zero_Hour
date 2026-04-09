# Generals/Code/Tools/mangler/wnet/udp.cpp

## Purpose
Implements a cross-platform UDP socket wrapper for network communication.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Handles platform-specific differences (Windows/Unix)
- Provides blocking/non-blocking mode control
- Supports socket buffer size configuration
- Implements select()-based waiting for network activity

## Key Types
- UDP (Class): Main UDP socket wrapper class
- sockStat (Enum): Socket error status codes

## Key Functions
### UDP::Bind(char *Host, uint16 port)
- Purpose: Binds UDP socket to host/port using hostname resolution
- Calls: Bind(uint32 IP, uint16 Port), gethostbyname(), inet_addr()

### UDP::Bind(uint32 IP, uint16 Port)
- Purpose: Binds UDP socket to specific IP address and port
- Calls: socket(), bind(), getsockname(), SetBlocking()

### UDP::Write(uint8 *msg, uint32 len, uint32 IP, uint16 port)
- Purpose: Sends UDP datagram to specified destination
- Calls: sendto(), ClearStatus()

### UDP::Read(uint8 *msg, uint32 len, sockaddr_in *from)
- Purpose: Receives UDP datagram with optional source address
- Calls: recvfrom()

### UDP::Wait(sint32 sec, sint32 usec, fd_set &returnSet)
- Purpose: Waits for network activity on this socket
- Calls: Wait(sint32 sec, sint32 usec, fd_set &givenSet, fd_set &returnSet)

### UDP::SetBlocking(bit8 block)
- Purpose: Configures socket blocking mode
- Calls: ioctlsocket() (Windows) or fcntl() (Unix)

## Globals
- None

## Dependencies
- Key includes: "udp.h", "wlib/wdebug.h"
- External symbols: socket(), bind(), sendto(), recvfrom(), select(), gethostbyname(), inet_addr(), WSAGetLastError(), errno, FD_SET, FD_ISSET, FD_ZERO
- Platform-specific: Windows Sockets API (WSA*) and POSIX socket functions
