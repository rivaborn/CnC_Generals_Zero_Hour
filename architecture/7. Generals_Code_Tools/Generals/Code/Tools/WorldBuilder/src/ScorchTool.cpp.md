# Generals/Code/Tools/WorldBuilder/src/ScorchTool.cpp

## Purpose
Implements the scorch tool functionality in WorldBuilder, allowing users to place and manipulate scorch marks on the terrain.

## Responsibilities
- Handles scorch mark placement and selection
- Manages scorch tool activation/deactivation
- Updates scorch options panel
- Processes mouse input for scorch operations

## Key Types
- **ScorchTool (Class)**: Main tool class for scorch functionality
- **ScorchOptions (Class)**: Manages scorch tool settings (external)

## Key Functions
### ScorchTool::pickScorch
- Purpose: Finds the nearest scorch mark at the given location
- Calls: MapObject::getFirstMapObject, MapObject::isScorch, MapObject::getLocation

### ScorchTool::mouseDown
- Purpose: Handles mouse down event for scorch placement/selection
- Calls: pickScorch, newInstance, MapObject::setSelected, MapObject::setIsScorch, AddObjectUndoable constructor

### ScorchTool::mouseMoved
- Purpose: Handles mouse movement for scorch tool feedback
- Calls: pickScorch

## Globals
- None

## Dependencies
- "StdAfx.h", "resource.h", "ScorchTool.h", "PointerTool.h", "CUndoable.h", "WHeightMapEdit.h", "WorldBuilderDoc.h", "WorldBuilderView.h", "ScorchOptions.h", "MainFrm.h", "DrawObject.h", "Common/WellKnownKeys.h"
- MapObject, CMainFrame, AddObjectUndoable, Coord3D, WbView, CWorldBuilderDoc
