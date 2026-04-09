# Generals/Code/Tools/WorldBuilder/src/RampTool.cpp

## Purpose
Implements the ramp tool for terrain editing in WorldBuilder, allowing users to create height ramps between two points.

## Responsibilities
- Handles mouse input for ramp creation
- Applies height changes to the terrain
- Manages visual feedback during ramp creation
- Integrates with the undo system for terrain modifications

## Key Types
- **RampTool (Class)**: Main class implementing the ramp tool functionality
- **Coord3D (Struct)**: Represents 3D coordinates
- **VecHeightMapIndexes (Type)**: Collection of height map indexes

## Key Functions
### `activate`
- Purpose: Activates the ramp tool and shows the options dialog
- Calls: `Tool::activate`, `CMainFrame::GetMainFrame()->showOptionsDialog`

### `mouseMoved`
- Purpose: Handles mouse movement for ramp creation and feedback
- Calls: `applyRamp`, `drawFeedback`, `TheTerrainRenderObject->getHeightMapHeight`

### `applyRamp`
- Purpose: Applies the ramp height changes to the terrain
- Calls: `duplicate`, `BuildRectFromSegmentAndWidth`, `getAllIndexesIn`, `ShortestDistancePointToSegment2D`, `pDoc->updateHeightMap`, `pDoc->AddAndDoUndoable`

## Globals
- **TheRampOptions (Type)**: Global ramp tool options
- **TheTerrainRenderObject (Type)**: Global terrain render object

## Dependencies
- Key includes: `StdAfx.h`, `RampTool.h`, `CUndoable.h`, `MainFrm.h`, `DrawObject.h`, `RampOptions.h`, `Resource.h`, `WbView.h`, `WHeightMapEdit.h`, `WorldBuilder.h`, `WorldBuilderDoc.h`, `GameClient/Line2
