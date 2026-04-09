# Generals/Code/Tools/WorldBuilder/include/EditCoordParameter.h

## Purpose
Header for a dialog class used to edit coordinate parameters in the WorldBuilder tool.

## Responsibilities
- Define the `EditCoordParameter` dialog class for coordinate editing
- Manage data exchange between UI and internal coordinate representation
- Handle dialog initialization and user input validation

## Key Types
- **EditCoordParameter (Class)**: Dialog for editing coordinate parameters
- **SidesList (Class)**: Forward-declared class for side management
- **(anonymous enum) (Enum)**: Contains `IDD` enum value for dialog resource ID
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### EditCoordParameter::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: `CDataExchange` methods

### EditCoordParameter::OnInitDialog
- Purpose: Initializes the dialog when it's created
- Calls: Not inferable

### EditCoordParameter::OnOK
- Purpose: Handles OK button click to validate and save changes
- Calls: Not inferable

### EditCoordParameter::OnCancel
- Purpose: Handles cancel button click to discard changes
- Calls: Not inferable

## Globals
- **m_parameter (Parameter**)**: Pointer to the parameter being edited
- **m_coord (Coord3D)**: Stores the coordinate value being edited

## Dependencies
- `"GameLogic/Scripts.h"` for `Parameter` type
- `SidesList` class (forward-declared)
- MFC classes: `CDialog`, `CDataExchange`, `CWnd`
- Windows dialog resource system (`IDD` enum)
