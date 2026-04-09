# Generals/Code/Tools/WorldBuilder/include/TeamIdentity.h

## Purpose
Header for the TeamIdentity dialog class used in WorldBuilder for team configuration.

## Responsibilities
- Manages team properties in the WorldBuilder UI
- Handles team unit assignments and production settings
- Provides data exchange for team attributes
- Processes team-related UI events

## Key Types
- **TeamIdentity (Class)**: Dialog for team configuration in WorldBuilder
- **Dict (Class)**: Reference to team dictionary data
- **SidesList (Class)**: Reference to sides list data
- **(anonymous enum) (Enum)**: Contains IDD constant
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### TeamIdentity()
- Purpose: Standard constructor for TeamIdentity dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles DDX/DDV data exchange for dialog controls
- Calls: None

### OnCommand()
- Purpose: Processes WM_COMMAND messages for the dialog
- Calls: None

### loadUnitsInfo()
- Purpose: Loads unit information for a range of unit types
- Calls: None

### OnUnitTypeButton()
- Purpose: Handles unit type button click events
- Calls: None

### setTeamDict()
- Purpose: Sets the team dictionary reference
- Calls: None

### setSidesList()
- Purpose: Sets the sides list reference
- Calls: None

## Globals
- None

## Dependencies
- CPropertyPage (MFC)
- CDataExchange (MFC)
- Dict (forward declared)
- SidesList (forward declared)
- NameKeyType (external type)
- IDD_TeamIdentity (resource ID)
