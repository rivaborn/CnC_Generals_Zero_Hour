# Generals/Code/Tools/mangler/wnet/udp.h

## Purpose
Defines a cross-platform UDP socket wrapper class for network communication.

## Responsibilities
- Manages UDP socket creation, binding, and I/O operations
- Provides error handling via a custom `sockStat` enum
- Supports both blocking and non-blocking modes
- Handles platform-specific socket APIs (Windows/Unix)

## Key Types
- **UDP (Class)**: Wrapper for UDP socket operations
- **sockStat (Enum)**: Error status codes for socket operations

## Key Functions
### `UDP::Bind`
- Purpose: Binds the socket to a specific IP and port
- Calls: Platform-specific socket APIs

### `UDP::Write`
- Purpose: Sends data over UDP to a specified address
- Calls: Platform-specific sendto()

### `UDP::Read`
- Purpose: Receives data from the socket
- Calls: Platform-specific recvfrom()

### `UDP::Wait`
- Purpose: Waits for socket activity using select()
- Calls: Platform-specific select()

## Globals
- **None**

## Dependencies
- Platform-specific headers (winsock.h, sys/socket.h, etc.)
- `<wlib/wstypes.h>`, `<wlib/wtime.h>` for types and timing
- Standard C headers (stdio.h, errno.h, etc.)
