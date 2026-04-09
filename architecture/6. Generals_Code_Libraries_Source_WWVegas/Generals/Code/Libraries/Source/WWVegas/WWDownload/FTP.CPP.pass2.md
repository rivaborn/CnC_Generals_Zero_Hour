# Generals/Code/Libraries/Source/WWVegas/WWDownload/FTP.CPP - Enhanced Analysis

## Architectural Role
This file implements the FTP client subsystem responsible for downloading game content (maps, mods, updates) from remote servers. It bridges the networking layer (WinSock) with the file system and registry for persistent download state management.

## Cross-References
### Incoming
- Likely called from: `Generals/Code/Game/Source/DownloadManager.cpp` (main download orchestration), `Generals/Code/Game/Source/UI/DownloadDialog.cpp` (UI feedback), and potentially mod loading systems.

### Outgoing
- Calls into: WinSock API (`socket`, `connect`, `recv`, `send`), Windows Registry API (`RegOpenKeyEx`, `RegQueryValueEx`), and file system functions (`fopen`, `fseek`).

## Design Patterns
- **State Machine**: Uses status flags (e.g., `FTPSTAT_CONNECTING`, `FTPSTAT_LOGGEDIN`) to manage FTP protocol state transitions.
- **Registry Persistence**: Stores download metadata in the Windows Registry for resumable downloads.
- **Non-blocking I/O**: Implements a workaround for firewalls via registry-checkable non-blocking mode.

*Not inferable*: Exact threading model (gThreadFlag suggests async hostname resolution, but no thread management code visible).
