# GeneralsMD/Code/GameEngine/Source/GameNetwork/FileTransfer.cpp - Enhanced Analysis

## Architectural Role
This file implements the file transfer subsystem for multiplayer map distribution, bridging the networking layer (TheNetwork) with the UI layer (LoadScreen/Shell). It handles the orchestration of file transfers, progress tracking, and path manipulation for map-related assets.

## Cross-References
### Incoming
- Likely called from game initialization/loading code when a multiplayer game starts and map files need to be distributed
- May be invoked by the matchmaking/join game flow when connecting to a host with custom maps

### Outgoing
- **TheNetwork**: Core networking interface for actual file transfer operations
- **LoadScreen**: UI component for displaying transfer progress
- **Shell**: Main game window management for hiding/showing during transfers

## Design Patterns
- **Facade Pattern**: The file presents a simplified interface (DoAnyMapTransfers) that hides the complexity of individual file transfers and progress tracking
- **Strategy Pattern**: Different file types (preview, INI, etc.) are handled by separate path construction functions, allowing for easy extension
- **Observer Pattern**: Progress updates are pushed to the LoadScreen UI component during transfers

Rules followed. Output under 400 tokens.
