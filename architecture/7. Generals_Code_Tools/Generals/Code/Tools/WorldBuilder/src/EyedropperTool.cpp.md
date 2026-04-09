# Generals/Code/Tools/WorldBuilder/src/EyedropperTool.cpp

## Purpose
Implements the eyedropper tool for the WorldBuilder editor, allowing users to sample terrain textures.

## Responsibilities
- Activates the terrain material options panel
- Handles mouse input to sample texture classes
- Updates the terrain material panel with sampled textures
- Disables brush feedback during operation

## Key Types
- EyedropperTool (class): Main tool class for texture sampling
- None

## Key Functions
### EyedropperTool::activate
- Purpose: Shows the terrain materials options panel and configures tool options
- Calls: CMainFrame::GetMainFrame()->showOptionsDialog, TerrainMaterial::setToolOptions, DrawObject::setDoBrushFeedback

### EyedropperTool::mouseDown
- Purpose: Samples the texture class at the mouse position and sets it as the foreground texture
- Calls: pView->viewToDocCoords, pDoc->getCellIndexFromCoord, pMap->getTextureClass, TerrainMaterial::setFgTexClass

## Globals
- None

## Dependencies
- StdAfx.h, resource.h
- EyedropperTool.h, TerrainMaterial.h, WHeightMapEdit.h, WorldBuilderDoc.h, WorldBuilderView.h, MainFrm.h, DrawObject.h
- CMainFrame, CPoint, WbView, CWorldBuilderDoc, Coord3D, WorldHeightMapEdit, Int, TerrainMaterial, DrawObject
