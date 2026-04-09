# Generals/Code/GameEngine/Source/GameNetwork/FileTransfer.cpp - Enhanced Analysis

## Architectural Role
This file implements the file transfer subsystem for multiplayer map distribution, bridging the networking layer (TheNetwork) with the UI layer (MapTransferLoadScreen). It handles the orchestration of file transfers, progress tracking, and timeout management during map distribution.

## Cross-References
### Incoming
- Likely called from the game initialization flow (e.g., when a host starts a game or a client joins) to ensure all players have the required map files.
- Potentially invoked by the lobby/pre-game UI when a map is selected.

### Outgoing
- **TheNetwork**: Uses `sendFileAnnounce`, `sendFile`, `getFileTransferProgress`, and `areAllQueuesEmpty` for actual file transfer operations.
- **MapTransferLoadScreen**: Updates the UI with progress, timeouts, and filenames during transfers.
- **TheShell**: Temporarily hides/shows the shell UI during transfers.

## Design Patterns
- **Facade Pattern**: Abstracts the complexity of file transfers behind simple functions like `DoAnyMapTransfers`, hiding the details of progress tracking and timeouts.
- **Observer Pattern**: The load screen (`MapTransferLoadScreen`) is updated incrementally as the transfer progresses, acting as an observer to the transfer state.
- **Strategy Pattern**: The file transfer logic is modular, with separate functions for constructing paths (`GetPreviewFromMap`, etc.), allowing for flexibility in file handling.
