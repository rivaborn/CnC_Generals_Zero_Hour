# Generals/Code/Tools/WorldBuilder/src/BrushTool.cpp

## Purpose
Implements a brush tool for terrain height editing in WorldBuilder, allowing users to paint height changes on the terrain map.

## Responsibilities
- Manages brush parameters (width, feather, height, shape)
- Handles mouse input for terrain editing
- Applies height changes to the heightmap
- Provides visual feedback during editing
- Manages undo/redo operations for brush actions

## Key Types
- **BrushTool (Class)**: Main brush tool implementation
- **WBDocUndoable (Class)**: Undoable command for brush operations
- **WorldHeightMapEdit (Class)**: Heightmap data structure

## Key Functions
### setHeight
- Purpose: Sets the brush height and notifies the options panel
- Calls: BrushOptions::setHeight

### setWidth
- Purpose: Sets the brush width and updates feedback parameters
- Calls: BrushOptions::setWidth, DrawObject::setBrushFeedbackParms

### setFeather
- Purpose: Sets the brush feather and updates feedback parameters
- Calls: BrushOptions::setFeather, DrawObject::setBrushFeedbackParms

### mouseDown
- Purpose: Initializes brush operation by copying the heightmap
- Calls: REF_PTR_RELEASE, duplicate, mouseMoved

### mouseUp
- Purpose: Finalizes brush operation and creates undo command
- Calls: REF_PTR_RELEASE, AddAndDoUndoable

### mouseMoved
- Purpose: Applies brush height changes at current position
- Calls: viewToDocCoords, getCenterIndex, calcSquareBlendFactor/calcRoundBlendFactor, setHeight, updateHeightMap

## Globals
- **m_brushWidth (Int)**: Current brush width
- **m_brushFeather (Int)**: Current brush feather amount
- **m_brushSquare (Bool)**: Brush shape flag (square/round)
- **m_brushHeight (Int)**: Current brush height value

## Dependencies
- "StdAfx.h", "resource.h", "BrushTool.h", "CUndoable.h", "MainFrm.h", "WHeightMapEdit.h", "WorldBuilderDoc.h", "WorldBuilderView.h", "BrushOptions.h", "DrawObject.h"
- CMainFrame, WbView, CWorldBuilderDoc, WorldHeightMapEdit, BrushOptions, DrawObject, WBDocUndoable, REF_PTR_RELEASE macro
