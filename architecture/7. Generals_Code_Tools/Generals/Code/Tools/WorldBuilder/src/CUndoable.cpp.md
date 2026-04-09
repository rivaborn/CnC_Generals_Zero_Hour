# Generals/Code/Tools/WorldBuilder/src/CUndoable.cpp

## Purpose
Implements undo/redo functionality for the WorldBuilder map editor, handling terrain, objects, and polygon triggers.

## Responsibilities
- Manages undo/redo operations for map edits
- Handles heightmap changes with object offsetting
- Tracks object additions/removals and modifications
- Manages polygon trigger edits (points, creation, deletion)
- Maintains selection state during undo operations

## Key Types
- **Undoable (Class)**: Base class for undoable operations
- **WBDocUndoable (Class)**: Handles heightmap and object offset undo/redo
- **AddObjectUndoable (Class)**: Manages object addition/removal
- **MoveInfo (Class)**: Tracks object movement/rotation changes
- **DeleteObjectUndoable (Class)**: Handles object deletion
- **AddPolygonUndoable (Class)**: Manages polygon trigger creation
- **ModifyPolygonPointUndoable (Class)**: Tracks polygon point modifications
- **MovePolygonUndoable (Class)**: Handles polygon movement
- **InsertPolygonPointUndoable (Class)**: Manages polygon point insertion
- **DeletePolygonPointUndoable (Class)**: Tracks polygon point deletion
- **DeletePolygonUndoable (Class)**: Handles polygon trigger deletion

## Key Functions
### Undoable::Do()
- Purpose: Execute the undoable operation
- Calls: None (virtual base)

### WBDocUndoable::Do()
- Purpose: Apply new heightmap and offset objects
- Calls: mPDoc->SetHeightMap, pCur->setLocation, pBuild->setLocation, mPDoc->invalObject

### AddObjectUndoable::Do()
- Purpose: Add objects to map and update layers
- Calls: PointerTool::clearSelection, pCur->validate, TheLayersList->addMapObjectToLayersList, m_pDoc->invalObject

### DeleteObjectUndoable::Do()
- Purpose: Delete selected objects and update views
- Calls: TheLayersList->removeMapObjectFromLayersList, pCur->DoDelete, p3View->resetRenderObjects, p3View->invalObjectInView

### MoveInfo::DoMove()
- Purpose: Apply movement/rotation changes to objects
- Calls: m_objectToModify->setLocation, m_objectToModify->setAngle, m_objectToModify->setThingTemplate, m_objectToModify->setName

## Globals
- None

## Dependencies
- CUndoable.h, PointerTool.h, RoadTool.h, WHeightMapEdit.h, WorldBuilderDoc.h
- GameLogic/PolygonTrigger.h, GameLogic/SidesList.h
- W3DDevice/GameClient/HeightMap.h, Common/Debug.h
- mapobjectprops.h, ObjectOptions.h, BuildList.h
- WbView3D.h, LayersList.h, Common/WellKnownKeys.h
- WorldBuilder.h, Common/UnicodeString.h
