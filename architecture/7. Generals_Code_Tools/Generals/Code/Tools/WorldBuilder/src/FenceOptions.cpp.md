# Generals/Code/Tools/WorldBuilder/src/FenceOptions.cpp

## Purpose
Handles fence object selection and configuration in the WorldBuilder editor.

## Responsibilities
- Manages fence object list and tree view display
- Updates object options panel based on selected fence
- Handles fence spacing and offset configuration
- Processes user input for fence selection and spacing changes

## Key Types
- **FenceOptions (class)**: Main dialog class for fence options panel
- **MapObject (struct)**: Represents objects in the world
- **ThingTemplate (struct)**: Template data for game objects

## Key Functions
### `updateObjectOptions`
- Purpose: Syncs selected fence object with ObjectOptions panel
- Calls: `ObjectOptions::selectObject`, `getThingTemplate`, `setWindowText`

### `OnInitDialog`
- Purpose: Initializes dialog controls and populates object list
- Calls: `TheThingFactory->firstTemplate`, `newInstance`, `addObject`, `Create`

### `OnNotify`
- Purpose: Handles tree view notifications (selection changes, expansion)
- Calls: `GetItem`, `SetItem`, `SelectItem`, `updateObjectOptions`

### `OnChangeFenceSpacingEdit`
- Purpose: Updates fence spacing when user edits the spacing field
- Calls: `GetWindowText`, `atof`

## Globals
- **m_staticThis (FenceOptions*)**: Singleton instance pointer
- **m_updating (Bool)**: Flag for update operations
- **m_currentObjectIndex (Int)**: Currently selected object index
- **m_fenceSpacing (Real)**: Current fence spacing value
- **m_fenceOffset (Real)**: Current fence offset value

## Dependencies
- `stdafx.h`, `resource.h`, `Lib\BaseType.h`
- `FenceOptions.h`, `ObjectOptions.h`, `WHeightMapEdit.h`
- `WorldBuilderDoc.h`, `CUndoable.h`
- `W3DDevice/GameClient/HeightMap.h`
- `Common/WellKnownKeys.h`, `Common/ThingTemplate.h`
- `Common/ThingFactory.h`, `Common/ThingSort.h`
- `GameLogic/SidesList.h`, `GameClient/Color.h`
- MFC classes (`CWnd`, `CDialog`, `CString`, etc.)
