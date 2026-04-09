# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/Download.cpp - Enhanced Analysis

## Architectural Role
This file implements the core download functionality for the game's patch/update system, bridging the networking layer (FTP) with the game's UI and resource management. It acts as a state machine controller for file transfers, handling progress reporting and error recovery.

## Cross-References
### Incoming
- Likely called from UI modules (e.g., patch dialogs) and the main game loop
- May be invoked by the modding system for custom content downloads

### Outgoing
- Directly uses `m_Ftp` (FTP client implementation)
- Notifies listeners (UI/other systems) via callback interface
- Depends on Windows API (`timeGetTime`, `_mkdir`, `_stat`)

## Design Patterns
- **State Pattern**: Download states (DOWNLOADSTATUS_*) are explicitly managed in PumpMessages()
- **Observer Pattern**: Listener callbacks decouple download logic from UI/progress reporting
- **Resource Management**: Handles file system operations and cleanup (e.g., `_mkdir("download")`)

*Not inferable*: Exact FTP implementation details or listener hierarchy.
