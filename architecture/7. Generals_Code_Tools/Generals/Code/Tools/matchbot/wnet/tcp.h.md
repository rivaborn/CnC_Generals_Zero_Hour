# Generals/Code/Tools/matchbot/wnet/tcp.h

## Purpose
TCP socket abstraction layer for cross-platform networking in the matchbot tool.

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
### TCP::Connect
- Purpose: Establish a TCP connection to a remote host
- Calls: Not inferable (implementation in .cpp)

### TCP::Write
- Purpose: Send data over the TCP connection
- Calls: Not inferable

### TCP::Read
- Purpose: Receive data from the TCP connection
- Calls: Not inferable

### TCP::Wait
- Purpose: Wait for socket activity with timeout
- Calls: Not inferable

## Globals
- **None**

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<errno.h>`, `<string.h>`, `<assert.h>`
- `<winsock.h>` (Windows) or `<sys/socket.h>` (Unix)
- `wlib/wstypes.h`, `wlib/wdebug.h`, `wlib/wtime.h`
