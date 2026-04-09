# Generals/Code/Tools/matchbot/wnet/tcp.cpp

## Purpose
Implements a cross-platform TCP networking class supporting both client and server modes with non-blocking sockets.

## Responsibilities
- Manages TCP connections (bind, connect, accept)
- Provides blocking/non-blocking read/write operations
- Handles socket state tracking and error status
- Supports server-side connection management with fd_set tracking
- Implements encapsulated write for proxy compatibility

## Key Types
- TCP (Class): Main TCP networking class handling client/server operations
- ConnectionState (Enum): Tracks socket connection state (CLOSED, CONNECTING, CONNECTED)
- Status (Enum): Socket error status codes (OK, INTR, INPROGRESS, etc.)

## Key Functions
### Write
- Purpose: Blocking write operation for TCP data
- Calls: SetBlocking, send

### WriteNB
- Purpose: Non-blocking write operation for TCP data
- Calls: send

### EncapsulatedWrite
- Purpose: Writes data with proxy-safe encoding (0â1,1â1,255â1,3)
- Calls: SetBlocking, send

### ConnectAsync
- Purpose: Initiates non-blocking connection attempt
- Calls: connect, IsConnected, Bind, GetStatus

### GetConnection
- Purpose: Server-side accept operation for new connections
- Calls: accept

### Wait
- Purpose: Waits for socket activity using select()
- Calls: select, FD_ISSET

## Globals
- None

## Dependencies
- tcp.h (header)
- stdarg.h (for variadic functions)
- errno.h (non-Windows error handling)
- Winsock API (Windows-specific socket functions)
- POSIX socket API (non-Windows)
- fd_set manipulation macros (FD_ZERO, FD_SET, etc.)
