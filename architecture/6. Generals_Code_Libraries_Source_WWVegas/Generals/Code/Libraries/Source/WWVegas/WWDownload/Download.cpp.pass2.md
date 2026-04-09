# Generals/Code/Libraries/Source/WWVegas/WWDownload/Download.cpp - Enhanced Analysis

## Architectural Role
This file implements the core download functionality for the game, handling FTP-based file transfers with progress tracking and resume capabilities. It bridges the game's content delivery system with the underlying network stack, ensuring patches and updates can be downloaded efficiently.

## Cross-References
### Incoming
- Likely called from the game's update/patching system (e.g., `Generals/Code/Game/Update/UpdateManager.cpp`)
- Possibly invoked by the main menu or loading screen when checking for updates

### Outgoing
- Uses `m_Ftp` (FTP client wrapper) for network operations
- Notifies a listener interface (callback-based) for progress/error reporting
- Depends on Windows API (`mmsystem.h`, `_mkdir`, `_stat`) for timing and filesystem operations

## Design Patterns
- **State Machine**: Download process is driven by `m_Status` enum, with `PumpMessages()` advancing states
- **Observer**: Listener pattern for progress/error notifications (decouples download logic from UI)
- **Strategy**: Resume logic uses `OnQueryResume()` callback to delegate resume decision to caller

*Not inferable*: Exact FTP implementation details or listener interface definition.
