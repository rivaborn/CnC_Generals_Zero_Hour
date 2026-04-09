# GeneralsMD/Code/GameEngine/Source/GameLogic/Map/PolygonTrigger.cpp - Enhanced Analysis

## Architectural Role
This file implements the core polygon trigger system, bridging map geometry with game logic. It's critical for spatial queries (e.g., point-in-polygon tests) and serialization, supporting both gameplay triggers and water/river mechanics.

## Cross-References
### Incoming
- **Map loading/saving**: `ParsePolygonTriggersDataChunk`/`WritePolygonTriggersDataChunk` called during map I/O.
- **AI/pathfinding**: `pointInTrigger` used for area-based logic (e.g., water avoidance).
- **UI/selection**: `getCenterPoint`/`getRadius` for trigger visualization.

### Outgoing
- **Terrain system**: `TheTerrainLogic->getGroundHeight` for Z-coordinate calculations.
- **Serialization**: `Xfer` class for save/load operations.
- **Memory management**: Direct `NEW`/`delete[]` usage (no pool allocation).

## Design Patterns
- **Singleton-like list management**: Global `ThePolygonTriggerListPtr` with static methods (`getFirstPolygonTrigger`, `deleteTriggers`).
- **Linked list**: Triggers chained via `m_nextPolygonTrigger` (manual memory management).
- **Bounds caching**: Lazy `m_boundsNeedsUpdate` flag with `updateBounds` (optimization for static triggers).
