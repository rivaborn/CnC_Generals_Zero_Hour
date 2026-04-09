# Generals/Code/Tools/WorldBuilder/include/TeamReinforcement.h

## Purpose
Defines the `TeamReinforcement` dialog class for the WorldBuilder tool, handling team reinforcement configuration.

## Responsibilities
- Manages team reinforcement settings via a property page.
- Handles UI events for reinforcement options (transport, veterancy, waypoints).
- Stores and updates team reinforcement data using a `Dict` object.
- Initializes dialog controls and message mappings.

## Key Types
- **TeamReinforcement (Class)**: Dialog for configuring team reinforcements in WorldBuilder.
- **(anonymous enum) (Enum)**: Contains `IDD` enum value for dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### `TeamReinforcement()`
- Purpose: Standard constructor for the dialog.
- Calls: None.

### `DoDataExchange(CDataExchange* pDX)`
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: None (framework method).

### `setTeamDict(Dict *pDict)`
- Purpose: Sets the team reinforcement data dictionary.
- Calls: None.

### `OnDeployBy()`
- Purpose: Handles deployment method selection.
- Calls: None.

### `OnTeamStartsFull()`
- Purpose: Handles team full status toggle.
- Calls: None.

### `OnSelchangeTransportCombo()`
- Purpose: Handles transport selection changes.
- Calls: None.

### `OnTransportsExit()`
- Purpose: Handles transport exit logic.
- Calls: None.

### `OnSelchangeVeterancy()`
- Purpose: Handles veterancy level selection.
- Calls: None.

### `OnSelchangeWaypointCombo()`
- Purpose: Handles waypoint selection changes.
- Calls: None.

### `OnInitDialog()`
- Purpose: Initializes dialog controls.
- Calls: None.

##
