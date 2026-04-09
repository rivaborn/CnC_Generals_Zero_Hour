# Generals/Code/Tools/WorldBuilder/src/FeatherTool.cpp

## Purpose
Implements a texture tiling/smoothing tool for the WorldBuilder editor, allowing users to feather (blend) heightmap data.

## Responsibilities
- Manages feather tool state (feather, rate, radius)
- Handles mouse input for brush operations
- Applies heightmap blending using feather parameters
- Manages undo/redo functionality for heightmap changes
- Updates document view with modified heightmap data

## Key Types
- `FeatherTool` (Class): Main tool class handling feather operations
- `FeatherOptions` (External): Options dialog for feather parameters
- `WorldHeightMapEdit` (External): Heightmap data structure

## Key Functions
### `activate()`
- Purpose: Shows brush options panel and sets up brush feedback
- Calls: `CMainFrame::GetMainFrame()`, `DrawObject::setDoBrushFeedback`, `DrawObject::setBrushFeedbackParms`

### `mouseDown()`
- Purpose: Initializes tool operation by duplicating heightmap data
- Calls: `REF_PTR_RELEASE`, `duplicate()`, `getXExtent()`, `getYExtent()`, `getDataPtr()`, `mouseMoved()`

### `mouseMoved()`
- Purpose: Applies feather blending at current mouse position
- Calls: `viewToDocCoords()`, `getCenterIndex()`, `calcRoundBlendFactor()`, `getHeight()`, `setHeight()`, `invalCell()`, `updateHeightMap()`

### `mouseUp()`
- Purpose: Finalizes tool operation and creates undo command
- Calls: `new WBDocUndoable()`, `AddAndDoUndoable()`, `REF_PTR_RELEASE()`

## Globals
- `m_feather` (Int): Current feather amount
- `m_rate` (Int): Current feather rate
- `m_radius` (Int): Current feather radius
- `m_htMapEditCopy` (WorldHeightMapEdit*): Working copy of heightmap
- `m_htMapFeatherCopy` (WorldHeightMapEdit*): Original heightmap reference
- `m_htMapRateCopy` (WorldHeightMapEdit*): Feather rate data

## Dependencies
- `StdAfx.h`, `resource.h`, `FeatherTool.h`, `FeatherOptions.h`, `CUndoable.h`, `DrawObject.h`, `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`
- `Coord3D`, `CPoint`, `WbView`, `CWorldBuilderDoc`, `WBDocUndoable`, `IRegion2D`
