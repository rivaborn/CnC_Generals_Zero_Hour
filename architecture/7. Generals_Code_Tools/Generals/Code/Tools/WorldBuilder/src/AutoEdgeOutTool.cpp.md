# Generals/Code/Tools/WorldBuilder/src/AutoEdgeOutTool.cpp

## Purpose
Implements a texture tiling tool for WorldBuilder, allowing users to blend terrain edges automatically.

## Responsibilities
- Handles tool activation and UI display
- Processes mouse input to trigger edge blending
- Manages height map duplication and modification
- Creates undoable commands for document changes

## Key Types
- **AutoEdgeOutTool (class)**: Main tool class for edge blending functionality

## Key Functions
### AutoEdgeOutTool::activate()
- Purpose: Shows the brush options panel when the tool is activated
- Calls: `Tool::activate()`, `CMainFrame::GetMainFrame()->showOptionsDialog()`

### AutoEdgeOutTool::mouseDown()
- Purpose: Executes edge blending on mouse click by duplicating and modifying the height map
- Calls: `pView->viewToDocCoords()`, `pDoc->getCellIndexFromCoord()`, `pDoc->GetHeightMap()->duplicate()`, `htMapEditCopy->autoBlendOut()`, `pDoc->updateHeightMap()`, `new WBDocUndoable()`, `pDoc->AddAndDoUndoable()`

## Globals
- None

## Dependencies
- `StdAfx.h`, `resource.h`
- `AutoEdgeOutTool.h`, `CUndoable.h`, `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`
- `Tool`, `CMainFrame`, `WorldHeightMapEdit`, `BlendMaterial`, `IRegion2D`, `WBDocUndoable`
