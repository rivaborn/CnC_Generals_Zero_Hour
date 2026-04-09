# Generals/Code/Tools/WorldBuilder/src/PolygonTool.cpp

## Purpose
Implements the polygon editing tool for WorldBuilder, allowing creation and modification of polygon triggers in the map editor.

## Responsibilities
- Handles polygon selection, creation, and modification
- Manages undo/redo operations for polygon edits
- Implements snapping and point insertion logic
- Controls cursor behavior during polygon editing
- Integrates with the terrain material options panel

## Key Types
- `SNAP_DISTANCE` (Enum): Defines the snapping distance threshold (5 pixels)

## Key Functions
### `poly_pickPoly`
- Purpose: Determines if a point is inside a polygon trigger
- Calls: `pointInTrigger`

### `pickPolygon`
- Purpose: Finds the polygon trigger at a given screen location
- Calls: `poly_pickPoly`, `poly_pickPoint`

### `poly_snapToPoly`
- Purpose: Snaps a point to nearby polygon vertices
- Calls: `getPoint`, `length`

### `poly_pickPoint`
- Purpose: Finds the closest polygon vertex to a screen point
- Calls: `docToViewCoords`

### `poly_getInsertIndex`
- Purpose: Calculates where to insert a new point in a polygon
- Calls: `getPoint`, `getNumPoints`

### `poly_pickOnMouseDown`
- Purpose: Handles polygon selection on mouse down
- Calls: `pickPolygon`, `poly_pickPoly`

### `startMouseDown`
- Purpose: Initiates polygon creation or modification
- Calls: `newInstance`, `addPoint`, `setTriggerName`

### `deleteSelectedPolygon`
- Purpose: Removes the currently selected polygon or point
- Calls: `AddAndDoUndoable`

### `setCursor`
- Purpose: Updates cursor appearance based on editing state
- Calls: `LoadCursor`

### `mouseMoved`
- Purpose: Handles polygon dragging and point movement
- Calls: `viewToDocCoords`, `snapPoint`, `setPoint`

## Globals
- `m_poly_isActive` (Bool): Tracks if polygon tool is active
- `m_poly_isAdding` (Bool): Tracks if adding new polygon points
- `m_poly_curSelectedPolygon` (PolygonTrigger*): Currently selected polygon
- `m_poly_dragPointNdx` (Int): Index of dragged point (-1 if none)

## Dependencies
- `StdAfx.h`, `resource.h`, `PolygonTool.h`, `CUndoable.h`, `PointerTool.h`, `TerrainMaterial.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`, `WorldBuilderView.h`, `MainFrm.h`, `DrawObject.h`, `GameLogic/PolygonTrigger.h`,
