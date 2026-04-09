# GeneralsMD/Code/GameEngine/Include/GameLogic/TerrainLogic.h - Enhanced Analysis

## Architectural Role
This header defines the core terrain system interface, bridging between the logical game world and the physical representation. It manages navigation data (waypoints, bridges), terrain modifications, and water systems, serving as the central authority for spatial queries in pathfinding and collision systems.

## Cross-References
### Incoming
- Pathfinding subsystem (uses `getLayerHeight`, `getLayerForDestination`)
- AI movement logic (consumes waypoint and bridge data)
- Object placement/construction systems (calls `flattenTerrain`, `createCraterInTerrain`)
- Line-of-sight calculations (uses `isClearLineOfSight`)

### Outgoing
- **W3D Rendering**: Uses `Drawable` for bridge picking (`pickBridge`)
- **Water System**: Interfaces with `WaterHandle` for water table management
- **Object System**: References `Object` for bridge/object interactions
- **Serialization**: Uses `Xfer` for snapshot save/load

## Design Patterns
- **Singleton Pattern**: `TheTerrainLogic` provides global access to terrain state
- **Composite Pattern**: Waypoints form a linked list with directed graph connections
- **Observer Pattern**: Bridge damage state tracking via `m_bridgeDamageStatesChanged` flag

*Not inferable*: Exact implementation of pathfinding layer management or water grid updates.
