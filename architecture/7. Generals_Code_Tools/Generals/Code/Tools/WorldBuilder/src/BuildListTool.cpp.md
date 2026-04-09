# Generals/Code/Tools/WorldBuilder/src/BuildListTool.cpp

## Purpose
Implements the BuildListTool class for placing and manipulating buildings in WorldBuilder.

## Responsibilities
- Manages building placement and manipulation UI
- Handles mouse input for building selection/movement/rotation
- Integrates with PickUnitDialog for building selection
- Updates 3D view rendering during operations
- Maintains tool state and cursor feedback

## Key Types
- **BuildListTool (Class)**: Main tool class for building manipulation
- **PickUnitDialog (Class)**: Dialog for selecting buildings to place
- **BuildListInfo (Class)**: Represents a placed building instance

## Key Functions
### `createWindow`
- Purpose: Creates the PickUnitDialog window for building selection
- Calls: `SetAllowableType`, `SetFactionOnly`, `Create`, `SetupAsPanel`, `SetWindowPos`

### `activate`
- Purpose: Activates the tool and shows relevant UI panels
- Calls: `showOptionsDialog`, `update`, `resetRenderObjects`, `invalObjectInView`, `createWindow`, `ShowWindow`

### `mouseDown`
- Purpose: Handles mouse down events for building selection/movement
- Calls: `viewToDocCoords`, `pickedBuildObjectInView`, `setSelectedBuildList`, `clearSelection`

### `mouseMoved`
- Purpose: Handles mouse movement for building manipulation
- Calls: `viewToDocCoords`, `setObjTracking`, `calcAngle`, `setAngle`, `setLocation`, `invalBuildListItemInView`

### `mouseUp`
- Purpose: Handles mouse up events for building placement
- Calls: `viewToDocCoords`, `snapPoint`, `calcAngle`, `addBuilding`

## Globals
- **m_isActive (Bool)**: Tracks if tool is active
- **m_static_pickBuildingDlg (PickUnitDialog*)**: Static reference to building selection dialog

## Dependencies
- Key includes: `StdAfx.h`, `resource.h`, `BuildListTool.h`, `CUndoable.h`, `DrawObject.h`, `MainFrm.h`, `ObjectTool.h`, `PointerTool.h`, `PickUnitDialog.h`, `WbView3D.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`, `GameLogic/SidesList.h`
- External symbols: `Tool`, `BuildList`, `ObjectOptions`, `CMainFrame`, `CWorldBuilderDoc`, `WbView3d`, `WbView`, `MapObject`, `Coord3D`, `Real`
