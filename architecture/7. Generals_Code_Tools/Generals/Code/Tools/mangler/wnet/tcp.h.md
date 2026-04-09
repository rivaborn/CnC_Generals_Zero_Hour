# Generals/Code/Tools/mangler/wnet/tcp.h

## Purpose
Defines a cross-platform TCP socket wrapper class for network communication.

## Responsibilities
- Manages TCP client/server connections
- Provides I/O operations (read/write) with blocking/non-blocking modes
- Handles connection states and error conditions
- Supports both synchronous and asynchronous operations

## Key Types
- **TCP (Class)**: Cross-platform TCP socket wrapper
- **ConnectionState (Enum)**: Tracks connection state (CLOSED/CONNECTING/CONNECTED)
- **Anonymous enums**: Define mode flags (CLIENT/SERVER) and error codes

## Key Functions
### TCP(int newMode)
- Purpose: Constructor for TCP client/server
- Calls: Not inferable

### Bind(uint32 IP, uint16 port)
- Purpose: Binds socket to specified IP/port
- Calls: Not inferable

### Connect(uint32 IP, uint16 port)
- Purpose: Establishes connection to remote host
- Calls: Not inferable

### Write(const uint8 *msg, uint32 len)
- Purpose: Writes data to socket
- Calls: Not inferable

### Read(uint8 *msg, uint32 len)
- Purpose: Reads data from socket
- Calls: Not inferable

### Wait(sint32 sec, sint32 usec, fd_set &returnSet)
- Purpose: Waits for socket activity with timeout
- Calls: Not inferable

## Globals
- None

## Dependencies
- Platform-specific socket headers (winsock.h/unix sockets)
- WLib utilities (wstypes.h, wdebug.h, wtime.h)
- Standard C libraries (stdio.h, string.h, etc.)
