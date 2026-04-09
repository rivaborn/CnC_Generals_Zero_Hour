# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/Download.h - Enhanced Analysis

## Architectural Role
This file defines the core download infrastructure for the game, enabling FTP-based file transfers with progress tracking and callback notifications. It bridges the game's content delivery system with external FTP servers, critical for mod distribution and patching.

## Cross-References
### Incoming
- Likely called by UI components (e.g., download progress dialogs) and mod management systems.
- May be invoked by the game's update/patching mechanism.

### Outgoing
- Uses `Cftp` (from `ftp.h`) for low-level FTP operations.
- Relies on `downloaddefs.h` for status constants and enums.

## Design Patterns
- **Observer Pattern**: `IDownload` interface allows listeners to react to download events (progress, errors).
- **State Pattern**: Download status transitions (e.g., `DOWNLOADSTATUS_NONE`) are managed internally.
- **Resource Management**: Ownership of `Cftp` is explicitly handled in constructor/destructor.

*Not inferable: Specific callback implementations or error handling strategies.*
