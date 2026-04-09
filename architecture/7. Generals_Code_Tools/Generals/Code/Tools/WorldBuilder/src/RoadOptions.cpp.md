# Generals/Code/Tools/WorldBuilder/src/RoadOptions.cpp

## Purpose
Handles road editing options in the WorldBuilder tool, managing road types, corner styles, and selection logic.

## Responsibilities
- Manages road type selection via tree view
- Handles road corner style options (angled/tight/broad curves)
- Applies road modifications to selected objects
- Maintains road selection state and updates UI accordingly

## Key Types
- RoadOptions (Class): Main dialog class for road options
- TerrainRoadType (External): Road type definition
- ModifyFlagsUndoable (External): Undoable action for flag modifications

## Key Functions
### OnInitDialog
- Purpose: Initializes the dialog and loads road/bridge definitions
- Calls: addRoad, findOrAdd, setRoadTreeViewSelection, updateLabel

### updateSelection
- Purpose: Updates UI controls based on current road selection
- Calls: GetDlgItem, SetCheck

### applyToSelection
- Purpose: Applies road corner flags to selected objects
- Calls: ModifyFlagsUndoable constructor, AddAndDoUndoable

### ChangeRoadType
- Purpose: Changes road type for connected road segments
- Calls: SelectConnected, ModifyObjectUndoable constructor

## Globals
- m_staticThis (RoadOptions*): Singleton instance reference
- m_currentRoadName (AsciiString): Currently selected road name
- m_currentRoadIndex (Int): Index of current road in list
- m_numberOfRoads (Int): Total road count
- m_numberOfBridges (Int): Total bridge count
- m_angleCorners (Bool): Angle corner flag
- m_tightCurve (Bool): Tight curve flag
- m_doJoin (Bool): Road join flag

## Dependencies
- "RoadOptions.h", "CUndoable.h", "WHeightMapEdit.h", "WorldBuilderDoc.h"
- "W3DDevice/GameClient/HeightMap.h", "Common/FileSystem.h"
- "GameClient/TerrainRoads.h"
- MFC classes (CWnd, CDialog, CButton)
- External symbols: TheTerrainRoads, MapObject, CWorldBuilderDoc
