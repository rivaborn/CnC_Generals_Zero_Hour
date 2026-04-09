# Generals/Code/Tools/WorldBuilder/src/BorderTool.cpp

## Purpose
Handles map boundary editing in WorldBuilder, allowing users to add and modify map borders.

## Responsibilities
- Manages mouse interactions for border creation/modification
- Converts screen coordinates to map coordinates
- Updates document boundaries based on user input
- Handles activation/deactivation of the tool

## Key Types
- **BorderTool (Class)**: Main tool class for border editing
- **ModificationType (Enum)**: Defines border modification modes (up/right/free)

## Key Functions
### `mouseMoved`
- Purpose: Updates border position during mouse movement
- Calls: `pDoc->getBoundary`, `pView->viewToDocCoords`, `pDoc->changeBoundary`

### `mouseDown`
- Purpose: Initiates border creation or modification on mouse click
- Calls: `pView->viewToDocCoords`, `pDoc->addBoundary`, `pDoc->findBoundaryNear`

### `mouseUp`
- Purpose: Finalizes border operation when mouse button released
- Calls: None

## Globals
- **BOUNDARY_PICK_DISTANCE (const long)**: Minimum distance for boundary selection

## Dependencies
- `BorderTool.h`, `DrawObject.h`, `MainFrm.h`, `WbView3d.h`, `WorldBuilderDoc.h`
- Uses `Tool`, `WbView`, `CWorldBuilderDoc` classes
- References `ID_BORDERTOOL`, `IDC_POINTER`, `IDD_NO_OPTIONS` resources
