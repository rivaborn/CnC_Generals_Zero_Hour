# Generals/Code/Tools/WorldBuilder/include/wbview.h

## Purpose
Defines the `WbView` class, a base view class for the WorldBuilder tool, handling user interaction and rendering.

## Responsibilities
- Manages mouse and keyboard input for map editing
- Controls visibility of map elements (objects, models, names, etc.)
- Handles coordinate transformations between view and document space
- Provides feedback for selection and editing operations
- Manages camera and lighting controls

## Key Types
- `WbView` (Class): Base view class for WorldBuilder, handles rendering and input
- `TPickedStatus` (Enum): Represents picking states (none, center, arrow)
- `CWorldBuilderDoc` (Class): Document class for WorldBuilder (forward declared)
- `BuildListInfo` (Class): Build list information (forward declared)

## Key Functions
### `mouseDown`
- Purpose: Handles mouse down events for tracking operations
- Calls: `constrainCenterPt`, `getTrackingHeightMap`

### `mouseMove`
- Purpose: Handles mouse movement during tracking operations
- Calls: `constrainCenterPt`, `getTrackingHeightMap`

### `mouseUp`
- Purpose: Handles mouse up events for tracking operations
- Calls: `constrainCenterPt`, `getTrackingHeightMap`

### `picked`
- Purpose: Determines the picking status of an object at a given point
- Calls: None visible in header

### `OnDraw`
- Purpose: Overridden to draw the view contents
- Calls: Not specified in header

## Globals
- `m_snapToGrid` (Bool): Static flag controlling grid snapping behavior

## Dependencies
- `Lib/BaseType.h`, `Tool.h`, `Common/Debug.h`, `Common/ThingSort.h`
- `CView`, `CDC`, `CPoint`, `CDumpContext`, `CCmdUI`, `CWnd` (MFC classes)
- `Vector3`, `Coord3D`, `WorldHeightMapEdit`, `MapObject`, `IRegion2D`, `EditorSortingType` (game-specific types)
