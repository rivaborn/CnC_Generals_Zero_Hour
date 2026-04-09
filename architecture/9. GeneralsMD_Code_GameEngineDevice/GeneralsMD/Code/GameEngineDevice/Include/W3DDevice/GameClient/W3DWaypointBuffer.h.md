# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWaypointBuffer.h

## Purpose
Manages rendering of waypoints in the 3D scene, ensuring they appear between terrain and game entities.

## Responsibilities
- Render waypoints after terrain but before structures/units
- Manage waypoint buffer resources
- Handle waypoint visibility in waypoint plotting mode
- Maintain line style for waypoint rendering

## Key Types
- **SegmentedLineClass (Class)**: Not inferable.
- **W3DWaypointBuffer (Class)**: Manages waypoint rendering and buffer resources.

## Key Functions
### W3DWaypointBuffer()
- Purpose: Constructor for waypoint buffer.
- Calls: Not inferable.

### ~W3DWaypointBuffer()
- Purpose: Destructor for waypoint buffer.
- Calls: Not inferable.

### drawWaypoints()
- Purpose: Renders waypoints in the scene.
- Calls: Not inferable.

### freeWaypointBuffers()
- Purpose: Releases waypoint buffer resources.
- Calls: Not inferable.

### setDefaultLineStyle()
- Purpose: Sets default styling for waypoint lines.
- Calls: Not inferable.

## Globals
- **m_waypointNodeRobj (RenderObjClass*)**: Render object for waypoints.
- **m_line (SegmentedLineClass*)**: Line object for waypoints.
- **m_texture (TextureClass*)**: Texture used for waypoints.

## Dependencies
- `always.h`, `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `shader.h`, `vertmaterial.h`, `BaseType.h`, `GameType.h`
- `RenderInfoClass`, `RenderObjClass`, `TextureClass`, `SegmentedLineClass`
