# Generals/Code/Tools/WorldBuilder/src/BlendEdgeTool.cpp

## Purpose
Implements a texture tiling tool for the WorldBuilder editor, allowing users to blend textures between tiles.

## Responsibilities
- Handles mouse input for texture blending operations
- Manages undo/redo functionality for blend operations
- Interfaces with the document and view for coordinate conversion
- Applies texture blending to the height map

## Key Types
- **BlendEdgeTool (Class)**: Main tool class for texture blending
- **Coord3D (Type)**: 3D coordinate structure
- **CPoint (Type)**: 2D point structure
- **WbView (Type)**: View class for WorldBuilder
- **CWorldBuilderDoc (Type)**: Document class for WorldBuilder
- **WorldHeightMapEdit (Type)**: Height map editing class
- **IRegion2D (Type)**: 2D region structure
- **WBDocUndoable (Type)**: Undoable action class

## Key Functions
### BlendEdgeTool::BlendEdgeTool
- Purpose: Constructor for the BlendEdgeTool class
- Calls: None

### BlendEdgeTool::~BlendEdgeTool
- Purpose: Destructor for the BlendEdgeTool class
- Calls: None

### BlendEdgeTool::mouseDown
- Purpose: Handles mouse down event to capture the starting position
- Calls: WbView::viewToDocCoords

### BlendEdgeTool::mouseUp
- Purpose: Handles mouse up event to perform texture blending between tiles
- Calls: CWorldBuilderDoc::getCellIndexFromCoord, WorldHeightMapEdit::duplicate, WorldHeightMapEdit::blendTile, CWorldBuilderDoc::updateHeightMap, CWorldBuilderDoc::AddAndDoUndoable

## Globals
- None

## Dependencies
- StdAfx.h, resource.h
-
