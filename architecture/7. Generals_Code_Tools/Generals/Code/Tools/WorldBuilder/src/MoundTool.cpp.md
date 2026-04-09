# Generals/Code/Tools/WorldBuilder/src/MoundTool.cpp

## Purpose
Implements the mound/dig tool for terrain editing in WorldBuilder, allowing height adjustments with brush-based operations.

## Responsibilities
- Manages brush parameters (width, feather, height)
- Handles mouse input for terrain modification
- Maintains undo/redo functionality for heightmap changes
- Calculates blending factors for smooth terrain transitions
- Updates the heightmap with modified terrain data

## Key Types
- `MoundTool` (Class): Main tool class for raising terrain
- `DigTool` (Class): Subclass for lowering terrain
- `CUndoable` (External): Base class for undoable operations

## Key Functions
### `setMoundHeight`
- Purpose: Updates the mound height and notifies dependent UI
- Calls: `MoundOptions::setHeight`, `DrawObject::setBrushFeedbackParms`

### `mouseMoved`
- Purpose: Applies terrain height changes based on brush parameters
- Calls: `calcRoundBlendFactor`, `pDoc->invalCell`, `pDoc->updateHeightMap`

### `calcRoundBlendFactor`
- Purpose: Calculates blending factor for smooth terrain transitions
- Calls: None (static method)

## Globals
- `m_moundHeight` (Int): Current height adjustment value
- `m_brushWidth` (Int): Current brush width
- `m_brushFeather` (Int): Current feather amount for soft edges

## Dependencies
- `StdAfx.h`, `resource.h`, `MoundTool.h`, `CUndoable.h`, `DrawObject.h`, `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`, `MoundOptions.h`
- `CMainFrame`, `WBDocUndoable`, `WorldHeightMapEdit`, `Coord3D`, `CPoint`, `WbView`, `CWorldBuilderDoc`, `IRegion2D`
