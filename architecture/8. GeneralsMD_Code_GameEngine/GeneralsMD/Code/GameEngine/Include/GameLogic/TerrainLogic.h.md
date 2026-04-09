# GeneralsMD/Code/GameEngine/Include/GameLogic/TerrainLogic.h

## Purpose
Header file defining the TerrainLogic class and related structures for terrain representation and manipulation in the game.

## Responsibilities
- Manages terrain data, waypoints, bridges, and water tables
- Provides height queries and pathfinding support
- Handles terrain modifications (flattening, craters)
- Maintains logical terrain state for game simulation

## Key Types
- **Waypoint (Class)**: Represents navigation points with connections
- **Bridge (Class)**: Manages bridge objects and their properties
- **BridgeInfo (Class)**: Stores bridge geometry and state data
- **TerrainLogic (Class)**: Main terrain system interface
- **DynamicWaterEntry (Struct)**: Tracks water level changes over time

## Key Functions
### `getGroundHeight`
- Purpose: Returns terrain height at given coordinates
- Calls: Not inferable

### `findBridgeAt`
- Purpose: Locates bridge at specified position
- Calls: Not inferable

### `updateBridgeDamageStates`
- Purpose: Updates damage states for all bridges
- Calls: Not inferable

## Globals
- **TheTerrainLogic (TerrainLogic*)**: Singleton instance of terrain system

## Dependencies
- Common/GameMemory.h, Common/Snapshot.h, Common/STLTypedefs.h
- GameClient/TerrainRoads.h
- Uses MemoryPoolObject, Snapshot, SubsystemInterface base classes
- References Coord3D, Vector3, Matrix3D, WaterHandle types
