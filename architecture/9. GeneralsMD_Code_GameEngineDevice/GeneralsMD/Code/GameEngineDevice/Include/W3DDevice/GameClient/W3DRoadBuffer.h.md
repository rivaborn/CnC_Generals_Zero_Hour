# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DRoadBuffer.h

## Purpose
Header for the W3DRoadBuffer class, which manages rendering of roads in the game world.

## Responsibilities
- Define data structures for road segments, types, and rendering buffers
- Manage loading, drawing, and lighting of roads
- Handle road segment connections and intersections
- Maintain vertex and index buffers for road geometry

## Key Types
- **TRoadPt (Struct)**: Road point with location, top/bottom vectors, and flags
- **TRoadSegInfo (Struct)**: Road segment information including corners and offsets
- **TCorner (Enum)**: Road corner types (SEGMENT, CURVE, TEE, etc.)
- **RoadSegment (Class)**: Individual road segment with geometry and rendering data
- **RoadType (Class)**: Road texture and buffer management
- **W3DRoadBuffer (Class)**: Main road rendering system

## Key Functions
### loadRoads
- Purpose: Loads roads from map objects
- Calls: addMapObjects, insertCrossTypeJoins, insertCurveSegments, insertTeeIntersections

### drawRoads
- Purpose: Renders roads with terrain culling
- Calls: preloadRoadsInVertexAndIndexBuffers, loadLitRoadsInVertexAndIndexBuffers

### updateLighting
- Purpose: Updates diffuse lighting in road buffers
- Calls: RoadSegment::updateSegLighting

### insertTeeIntersections
- Purpose: Creates T-intersection road segments
- Calls: insertTee, insertY, insert4Way

### loadLitRoadsInVertexAndIndexBuffers
- Purpose: Loads lit roads into vertex/index buffers
- Calls: loadLitRoadSegment, loadLit4PtSection

## Globals
- **MAX_LINKS (const)**: Maximum road links (6)
- **DEFAULT_ROAD_SCALE (const)**: Default road scale (8.0f)
- **MIN_ROAD_SEGMENT (const)**: Minimum road segment length (0.25f)

## Dependencies
- "rendobj.h", "w3d_file.h", "dx8vertexbuffer.h", "dx8indexbuffer.h"
- "shader.h", "vertmaterial.h", "Common/FileSystem.h"
- "Lib/BaseType.h", "common/GameType.h", "Common/AsciiString.h"
- VertexFormatXYZDUV1, SphereClass, TextureClass, CameraClass
