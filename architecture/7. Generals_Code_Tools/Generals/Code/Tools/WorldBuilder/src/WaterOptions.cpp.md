# Generals/Code/Tools/WorldBuilder/src/WaterOptions.cpp

## Purpose
Handles water area configuration in the WorldBuilder editor, including height adjustment, river creation, and polygon management.

## Responsibilities
- Manages water height and spacing UI controls
- Handles polygon trigger selection and modification
- Implements river creation logic
- Provides undo/redo functionality for water edits
- Updates the 3D view when water properties change

## Key Types
- **WaterOptions (class)**: Main dialog class for water configuration
- **MovePolygonUndoable (class)**: Undoable action for polygon height changes
- **PolygonTrigger (class)**: Represents water/river areas in the map

## Key Functions
### `setHeight(Int height)`
- Purpose: Updates water height and UI display
- Calls: `GetDlgItem`, `SetWindowText`

### `updateTheUI()`
- Purpose: Refreshes UI controls based on current selection
- Calls: `GetDlgItem`, `SetWindowText`, `SetCheck`, `EnableWindow`

### `OnMakeRiver()`
- Purpose: Toggles river mode for selected polygon
- Calls: `GetDlgItem`, `GetCheck`, `setRiver`, `getSelectedPointNdx`, `getNumPoints`, `getPoint`, `setRiverStart`, `adjustCount`, `deletePoint`, `addPoint`, `deleteInstance`

### `adjustCount(PolygonTrigger *trigger, Int firstPt, Int lastPt, Int desiredPointCount)`
- Purpose: Adjusts polygon point density for rivers
- Calls: `newInstance`, `getNumPoints`, `getPoint`, `addPoint`, `setPoint`

### `startUpdateHeight()`
- Purpose: Initializes height adjustment undo action
- Calls: `getSingleSelectedPolygon`, `isWaterArea`, `getPoint`, `setPoint`, `new MovePolygonUndoable`, `AddAndDoUndoable`

### `updateHeight()`
- Purpose: Applies height offset to selected polygon
- Calls: `getSingleSelectedPolygon`, `SetOffset`, `Invalidate`

## Globals
- **m_staticThis (WaterOptions*)**: Singleton instance pointer
- **m_waterHeight (Int)**: Current water height value
- **m_waterPointSpacing (Int)**: Spacing between water points
- **m_creatingWaterAreas (Bool)**: Flag for water area creation mode
- **m_moveUndoable (MovePolygonUndoable*)**: Current undoable height adjustment
- **m_originalHeight (Int)**: Original height before adjustment
- **m_updating (Bool)**: Flag to prevent UI update loops

## Dependencies
- `stdafx.h`, `resource.h`, `BaseType.h`, `CUndoable.h`, `WaterOptions.h`, `WaypointOptions.h`, `WorldBuilder.h`, `WorldBuilderDoc.h`, `WbView3d.h`, `PolygonTool.h`, `WaypointTool.h`, `PolygonTrigger.h`, `WellKnownKeys.h`, `LayersList.h`
- `CDialog`, `CWnd`, `CComboBox`, `CButton`, `CString`, `AsciiString`, `ICoord3D`, `Real`, `Bool`, `Int`, `COptionsPanel`, `CWorldBuilderDoc`, `WbView3d`, `PolygonTrigger`, `MovePolygonUndoable`
