# Generals/Code/Tools/WorldBuilder/src/DrawObject.cpp

## Purpose
Handles rendering of objects, feedback, and UI elements in the WorldBuilder editor.

## Responsibilities
- Manages rendering of map objects, waypoints, and polygon triggers
- Provides visual feedback for tools (brushes, ramps, boundaries)
- Handles mesh mold visualization
- Updates vertex/index buffers for rendering
- Manages water rendering

## Key Types
- **DrawObject (Class)**: Main rendering class for WorldBuilder
- **WaterRenderObjClass (Class)**: Handles water rendering
- **Coord3D (Struct)**: 3D coordinate structure

## Key Functions
### `BuildRectFromSegmentAndWidth`
- Purpose: Creates a rectangular surface from a segment and width for ramp visualization
- Calls: `Vector3::Cross_Product`, `Vector3::Normalize`, `Vector3::Scale`

### `updateMeshVB`
- Purpose: Updates vertex buffer for mesh mold visualization
- Calls: `WW3DAssetManager::Create_Render_Obj`, `MeshClass::Get_Vertex_Count`, `MeshClass::Get_Vertex_Array`

### `Render`
- Purpose: Main rendering function that draws all objects and feedback
- Calls: `DX8Wrapper::Set_*`, `DX8Wrapper::Draw_Triangles`, `MapObject::getFirstMapObject`, `PolygonTrigger::getFirstPolygonTrigger`

### `setRampFeedbackParms`
- Purpose: Sets parameters for ramp feedback visualization
- Calls: None

## Globals
- **LINE_THICKNESS (Real)**: Line thickness constant
- **HANDLE_SIZE (Real)**: Handle size constant
- **m_brushWidth (Int)**: Current brush width
- **m_brushFeatherWidth (Int)**: Brush feather width
- **m_feedbackPoint (Coord3D)**: Current feedback point
- **m_rampStartPoint (Coord3D)**: Start point for ramp feedback
- **m_rampEndPoint (Coord3D)**: End point for ramp feedback
- **m_rampWidth (Real)**: Width of ramp feedback
- **m_dragWayStart (Coord3D)**: Start point for waypoint drag
- **m_dragWayEnd (Coord3D)**: End point for waypoint drag

## Dependencies
- DX8Wrapper.h, Mesh.h, Shader.h, Camera.h, RenderInfo.h
- WorldBuilder-specific headers (WBView3d.h, WorldBuilderDoc.h)
- Game logic headers (MapObject.h, PolygonTrigger.h)
- W3DDevice headers (W3DAssetManager.h, W3DWater.h)
