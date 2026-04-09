# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DGhostObject.cpp - Enhanced Analysis

## Architectural Role
This file implements the fog-of-war visualization system by maintaining "ghost" representations of objects that are obscured by fog. It bridges the game logic layer (Object/PartitionManager) with the rendering layer (W3DDevice), ensuring consistent visual state transitions when objects enter/exit fogged areas.

## Cross-References
### Incoming
- **GameLogic/Object.cpp**: Calls `snapShot()` when objects enter fog
- **PartitionManager.cpp**: Uses `registerGhostObject()` during spatial queries
- **Network/Xfer.cpp**: Calls `xfer()` for save/load synchronization

### Outgoing
- **W3DDevice/GameClient/W3DDisplay.cpp**: Calls `addToScene()` to render ghost objects
- **GameLogic/PartitionManager.cpp**: Calls `friend_setShroudednessPrevious()` to update fog state
- **WW3D2/Scene.cpp**: Uses W3D scene management for ghost object rendering

## Design Patterns
- **Snapshot Pattern**: `W3DRenderObjectSnapshot` captures and preserves object state at fog entry time
- **Proxy Pattern**: Ghost objects act as visual proxies for real objects in fogged areas
- **Observer Pattern**: Ghost objects monitor parent object state changes via `update()` calls

*Not inferable*: Exact synchronization mechanism with network layer (e.g., delta compression)
