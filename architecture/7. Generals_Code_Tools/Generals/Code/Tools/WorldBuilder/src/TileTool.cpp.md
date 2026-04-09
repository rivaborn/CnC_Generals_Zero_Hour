# Generals/Code/Tools/WorldBuilder/src/TileTool.cpp

## Purpose
Implements the TileTool and BigTileTool classes for terrain texture painting in WorldBuilder.

## Responsibilities
- Handles mouse input for texture painting
- Manages terrain material application
- Supports undo/redo functionality
- Provides brush feedback visualization
- Optimizes tile updates

## Key Types
- TileTool (Class): Base texture painting tool
- BigTileTool (Class): Extended tile tool with adjustable brush size
- TerrainMaterial (External): Manages texture material options

## Key Functions
### TileTool::activate()
- Purpose: Shows terrain material options panel and configures brush feedback
- Calls: CMainFrame::GetMainFrame(), showOptionsDialog(), TerrainMaterial::setToolOptions(), DrawObject::setDoBrushFeedback(), DrawObject::setBrushFeedbackParms()

### TileTool::mouseDown()
- Purpose: Initializes texture painting operation
- Calls: TerrainMaterial::getFgTexClass(), TerrainMaterial::getBgTexClass(), REF_PTR_RELEASE(), duplicate(), mouseMoved()

### TileTool::mouseMoved()
- Purpose: Applies textures along mouse movement path
- Calls: viewToDocCoords(), DrawObject::setFeedbackPos(), getCenterIndex(), setTileNdx(), updateHeightMap(), UpdateWindow()

### BigTileTool::setWidth()
- Purpose: Configures brush size for BigTileTool
- Calls: DrawObject::setBrushFeedbackParms()

## Globals
- m_currentWidth (Int): Stores current brush size for BigTileTool

## Dependencies
- StdAfx.h, resource.h, TileTool.h, CUndoable.h, MainFrm.h, WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h, BrushTool.h, DrawObject.h
- CMainFrame, TerrainMaterial, DrawObject, WorldHeightMapEdit, WbView, CWorldBuilderDoc, WBDocUndoable, Coord3D, IRegion2D, CPoint
