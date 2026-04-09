# Generals/Code/Tools/WorldBuilder/src/HandScrollTool.cpp

## Purpose
Implements a hand scrolling tool for the WorldBuilder editor, allowing camera movement and rotation.

## Responsibilities
- Handles mouse input for camera scrolling/rotation
- Manages scroll hysteresis and max scroll limits
- Resets camera on double-click
- Switches to pointer tool on right-click

## Key Types
- `HandScrollTool` (Class): Main tool class for hand scrolling functionality

## Key Functions
### `activate`
- Purpose: Placeholder for tool activation (does nothing for this tool)
- Calls: None

### `mouseDown`
- Purpose: Records initial mouse position and time for scroll tracking
- Calls: `::GetTickCount()`

### `mouseMoved`
- Purpose: Handles camera scrolling/rotation based on mouse movement
- Calls: `pView->viewToDocCoords`, `pView->rotateCamera`, `pView->scrollInView`

### `mouseUp`
- Purpose: Finalizes scroll actions or resets camera on double-click
- Calls: `pView->setDefaultCamera`, `pView->scrollInView`, `WbApp()->selectPointerTool`

## Globals
- `MAX_SCROLL` (Int): Maximum allowed scroll distance per frame

## Dependencies
- `StdAfx.h`, `resource.h`, `HandScrollTool.h`, `CUndoable.h`, `MainFrm.h`, `WHeightMapEdit.h`, `WorldBuilder.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`
- `Tool`, `CPoint`, `WbView`, `CWorldBuilderDoc`, `Coord3D`, `Real`, `Bool`
