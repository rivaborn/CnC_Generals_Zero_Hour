# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/ftp.h - Enhanced Analysis

## Architectural Role
This file defines the `Cftp` class, which is part of the game's download subsystem. It handles FTP client operations, enabling the game to download files (e.g., patches, mods) from remote servers. The class abstracts low-level socket operations and FTP protocol handling, providing a higher-level interface for file transfers.

## Cross-References
### Incoming
- `CDownload` (friend class) likely uses `Cftp` for file downloads.
- Other download-related components (e.g., patching system) may depend on `Cftp` for FTP operations.

### Outgoing
- Uses WinSock API for socket operations (`winsock.h`).
- Relies on `ftpdefs.h` for FTP-specific constants and types.
- Interacts with the file system via `FILE*` for local file operations.

## Design Patterns
- **Resource Management**: Uses RAII-like patterns for socket and file handles (e.g., `CloseSockets`, `CloseDataConnection`).
- **State Machine**: Manages FTP session state (e.g., `m_iStatus`, `m_iFilePos`) for resumable downloads.
- **Facade**: Hides FTP protocol complexity behind a simple interface (e.g., `ConnectToServer`, `GetNextFileBlock`).
