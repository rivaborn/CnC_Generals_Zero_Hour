# Generals/Code/Tools/WorldBuilder/src/MeshMoldTool.cpp

## Purpose
Implements a terrain shaping tool for WorldBuilder that applies 3D mesh molds to heightmaps.

## Responsibilities
- Handles mouse input for mesh molding operations
- Manages preview and application of heightmap changes
- Tracks tool state and updates visual feedback
- Creates undoable heightmap modifications

## Key Types
- **MeshMoldTool (Class)**: Main tool class for mesh molding
- **MeshMoldOptions (External)**: Stores tool configuration (scale, angle, height)
- **WorldHeightMapEdit (External)**: Heightmap data structure
- **Coord3D (Struct)**: 3D coordinate point
- **IRegion2D (Struct)**: 2D region definition

## Key Functions
### activate
- Purpose: Shows mesh mold options panel and initializes tool state
- Calls: CMainFrame::GetMainFrame(), showOptionsDialog

### deactivate
- Purpose: Cleans up tool resources and updates heightmap if previewing
- Calls: REF_PTR_RELEASE, CWorldBuilderDoc::GetActiveDoc(), updateHeightMap

### mouseDown
- Purpose: Starts mesh molding operation on left mouse button press
- Calls: WbView::viewToDocCoords, TheTerrainRenderObject::getHeightMapHeight, MeshMoldOptions::setHeight, DrawObject::setDoMeshFeedback, mouseMoved

### applyMesh
- Purpose: Applies mesh mold to heightmap using ray casting
- Calls: WorldHeightMapEdit::duplicate, SetCursor, DrawObject::peekMesh, MeshClass::Cast_Ray, CWorldBuilderDoc::updateHeightMap

### updateMeshLocation
- Purpose: Updates tool position and applies/removes preview
- Calls: DrawObject::setFeedbackPos, applyMesh, CWorldBuilderDoc::updateHeightMap

## Globals
- **m_tracking (Bool)**: Tracks if tool is active
- **m_toolPos (Coord3D)**: Current tool position
- **m_htMapEditCopy (WorldHeightMapEdit*)**: Working copy of heightmap

## Dependencies
- Key includes: StdAfx.h, MeshMoldTool.h, CUndoable.h, MainFrm.h, WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h, WorldBuilder.h, DrawObject.h, WbView3d.h, WW3D2/Mesh.h, WW3D2/MeshMdl.h, W3DDevice/GameClient/HeightMap.h
- External symbols: MeshMoldOptions, TheTerrainRenderObject, CMainFrame, CWorldBuilderDoc, DrawObject, WbView3d, MeshClass, RayCollisionTestClass, LineSegClass, Vector3, SphereClass
