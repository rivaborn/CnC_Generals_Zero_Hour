# Generals/Code/Tools/WorldBuilder/include/RoadOptions.h

## Purpose
Header file for the `RoadOptions` dialog class used in WorldBuilder to configure road properties.

## Responsibilities
- Manages road type selection and properties (curves, angles, joins)
- Handles UI interactions for road editing
- Maintains state for current road selection
- Provides methods to apply road changes to terrain

## Key Types
- **RoadOptions (Class)**: Dialog for road configuration in WorldBuilder
- **WorldHeightMapEdit (Class)**: External terrain editing class (forward declared)
- **(anonymous enum)**: Contains `NAME_MAX_LEN` constant
- **(anonymous enum)**: Contains `IDD` dialog resource ID

## Key Functions
### `DoDataExchange`
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: DDX/DDV framework calls

### `OnInitDialog`
- Purpose: Initializes the road options dialog
- Calls: Not inferable

### `OnTightCurve`, `OnAngled`, `OnBroadCurve`, `OnJoin`
- Purpose: Handle UI events for road shape options
- Calls: Not inferable

### `OnApplyRoad`
- Purpose: Applies selected road properties to terrain
- Calls: `applyToSelection`

### `addRoad`
- Purpose: Adds a road entry to the tree view
- Calls: `findOrAdd`

### `ChangeRoadType`
- Purpose: Changes the current road type
- Calls: Not inferable

### `applyToSelection`
- Purpose: Applies road properties to selected terrain
- Calls: Not inferable

## Globals
- **m_staticThis (RoadOptions*)**: Singleton instance pointer
- **m_updating (Bool)**: Flag for UI update state
- **m_currentRoadIndex (Int)**: Index of currently selected road
- **m
