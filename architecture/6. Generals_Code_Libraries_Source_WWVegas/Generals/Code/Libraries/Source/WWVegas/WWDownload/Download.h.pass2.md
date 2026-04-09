# Generals/Code/Libraries/Source/WWVegas/WWDownload/Download.h - Enhanced Analysis

## Architectural Role
This file defines the core download infrastructure for the game, enabling content updates and mod distribution via FTP. It bridges the game's resource management with external file operations, critical for post-launch content delivery.

## Cross-References
### Incoming
- Likely called by UI modules (e.g., patch/download screens) and resource managers when initiating content updates.
- May be referenced by modding tools or the game's update system.

### Outgoing
- Uses `Cftp` (from `ftp.h`) for low-level FTP operations.
- Relies on `downloaddefs.h` for status constants, suggesting shared state definitions across download-related components.

## Design Patterns
- **Observer Pattern**: `IDownload` interface enables decoupled progress/error reporting to listeners.
- **State Pattern**: Download status (`m_Status`) drives behavior, with `PumpMessages` likely handling state transitions.
- **Resource Management**: Manual memory handling for `Cftp` (RAII not used), typical of early 2000s C++.

*Not inferable*: Exact callback chain or threading model (e.g., if `PumpMessages` is called from a worker thread).
