# GeneralsMD/Code/GameEngine/Include/GameClient/MapUtil.h - Enhanced Analysis

## Architectural Role
This header bridges the filesystem, UI, and game logic layers by providing map metadata management and validation. It serves as the central interface for map-related operations, including caching, preview rendering, and multiplayer map transfer checks.

## Cross-References
### Incoming
- **UI System**: Calls `populateMapListbox` and `getMapPreviewImage` for map selection UI.
- **Game Lobby**: Uses `isValidMap` and `WouldMapTransfer` for multiplayer map validation.
- **Resource Manager**: Likely calls `parseMapPreviewChunk` during map loading.

### Outgoing
- **Filesystem**: Accesses map directories via `getMapDir`/`getUserMapDir`.
- **W3D Rendering**: Uses `Image` class for preview handling.
- **Data Chunk System**: Depends on `DataChunkInput` for map file parsing.

## Design Patterns
- **Singleton**: `TheMapCache` provides global access to cached map data.
- **Composite**: `MapCache` aggregates `MapMetaData` objects for hierarchical map storage.
- **Strategy**: `parseMapPreviewChunk` follows a callback pattern for chunk parsing.
