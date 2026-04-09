# GeneralsMD/Code/GameEngine/Source/GameLogic/Map/TerrainLogic.cpp

## Purpose
Handles logical terrain representation, including bridges, waypoints, and terrain modification for game objects.

## Responsibilities
- Manages terrain-based game objects (bridges, waypoints)
- Handles terrain flattening and crater creation
- Provides spatial queries (line/point in region)
- Manages water level updates over time
- Serialization/deserialization of terrain state

## Key Types
- **TerrainLogic (Class)**: Main terrain logic manager
- **Waypoint (Class)**: Represents navigation waypoints with links
- **Bridge (Class)**: Manages bridge objects and their towers
- **BridgeInfo (Struct)**: Stores bridge geometry and state data

## Key Functions
### LineInRegion
- Purpose: Checks if a line segment intersects a region
- Calls: PointInRegion2D, various geometry calculations

### PointInRegion2D
- Purpose: Tests if a 2D point lies within a polygon region
- Calls: None

### makeAlignToNormalMatrix
- Purpose: Creates a matrix aligned to a normal vector
- Calls: None

### flattenTerrain
- Purpose: Flattens terrain beneath structures
- Calls: TheTerrainVisual->setRawMapHeight, Point_In_Triangle_2D

### createCraterInTerrain
- Purpose: Creates craters in terrain
- Calls: TheTerrainVisual->setRawMapHeight

## Globals
- **TheTerrainLogic (TerrainLogic*)**: Global terrain logic instance

## Dependencies
- Common: DataChunk, GameState, MapObject, Radar, ThingFactory, ThingTemplate, WellKnownKeys, Xfer
- GameClient: TerrainVisual
- GameLogic: AI, AIPathfind, GameLogic, Damage, Object, PartitionManager, PolygonTrigger, Scripts, SidesList, TerrainLogic
- WWMath: plane, tri
