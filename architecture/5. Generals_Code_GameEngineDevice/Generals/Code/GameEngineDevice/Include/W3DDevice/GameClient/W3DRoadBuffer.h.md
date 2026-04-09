# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DRoadBuffer.h

## Purpose
Header file defining classes and structures for managing and rendering road segments in the game world.

## Responsibilities
- Defines data structures for road points, segments, and types
- Manages road rendering buffers and lighting
- Handles road segment generation and intersection logic
- Provides interface for loading and drawing roads

## Key Types
- **TRoadPt (Struct)**: Road point with location and connection info
- **TRoadSegInfo (Struct)**: Road segment geometric information
- **TCorner (Enum)**: Road segment types (segment, curve, intersections)
- **RoadSegment (Class)**: Individual road segment with vertex/index buffers
- **RoadType (Class)**: Road texture and rendering properties
- **W3DRoadBuffer (Class)**: Main road rendering manager

## Key Functions
### loadRoads
- Purpose: Loads roads from map objects list
- Calls: addMapObjects, insertCurveSegments, insertTeeIntersections, insertCrossTypeJoins

### drawRoads
- Purpose: Renders roads with terrain culling
- Calls: preloadRoadsInVertexAndIndexBuffers, applyTexture, draw

### updateLighting
- Purpose: Updates diffuse lighting in road buffers
- Calls: updateSegLighting for each segment

### preloadRoadsInVertexAndIndexBuffers
- Purpose: Fills index/vertex buffers for drawing
- Calls: preloadRoadSegment for each road type

## Globals
- **NUM_CORNERS (Enum)**: Number of road corners (4)
- **MAX_SEG_VERTEX/MAX_SEG_INDEX (Enum)**: Buffer size limits
- **DEFAULT_ROAD_SCALE/MIN_ROAD_SEGMENT (Const)**: Road rendering constants

## Dependencies
- DirectX 8 vertex/index buffer classes
- W3D rendering system (TextureClass, Shader)
- Math types (Vector2, SphereClass)
- File system and string utilities
