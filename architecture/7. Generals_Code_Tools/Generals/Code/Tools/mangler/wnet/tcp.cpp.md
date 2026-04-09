# Generals/Code/Tools/mangler/wnet/tcp.cpp

## Purpose
Implements a cross-platform TCP socket wrapper for client/server networking using non-blocking sockets.

## Responsibilities
- Manages TCP connections in client or server mode
- Provides blocking/non-blocking read/write operations
- Handles connection establishment and acceptance
- Supports socket status querying and error handling
- Implements connection encapsulation for proxy compatibility

## Key Types
- `TCP` (Class): Main TCP socket wrapper class
- `Wtime` (Class): Time utility for select() timeouts (external)
- `sockaddr_in` (Struct): Socket address structure (POSIX/Windows)

## Key Functions
### `TCP::Bind`
- Purpose: Binds socket to IP/port
- Calls: `socket()`, `SetBlocking()`, `setsockopt()`, `bind()`

### `TCP::Connect`
- Purpose: Establishes TCP connection (blocking)
- Calls: `connect()`, `GetStatus()`, `sleep_time` handling

### `TCP::ConnectAsync`
- Purpose: Initiates non-blocking TCP connection
- Calls: `connect()`, `GetStatus()`, `IsConnected()`

### `TCP::Write`
- Purpose: Sends data over socket (blocking)
- Calls: `SetBlocking()`, `send()`

### `TCP::Wait`
- Purpose: Waits for socket activity using select()
- Calls: `select()`, `FD_ISSET()`

### `TCP::GetConnection`
- Purpose: Accepts incoming client connections (server mode)
- Calls: `accept()`, `FD_SET()`

## Globals
- `addr` (sockaddr_in): Stores bound socket address
- `clientList` (fd_set): Tracks connected clients (server mode)
- `myIP`/`myPort` (uint32/uint16): Stores bound IP/port

## Dependencies
- `tcp.h` (header)
- POSIX sockets (`socket`, `bind`, `connect`, `accept`, `select`)
- Windows sockets (`WSAGetLastError`, `ioctlsocket`)
- `Wtime` class for timeouts
- `fd_set` operations (`FD_SET`, `FD_ISSET`, `FD_ZERO`)
