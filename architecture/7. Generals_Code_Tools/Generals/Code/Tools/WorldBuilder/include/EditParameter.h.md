# Generals/Code/Tools/WorldBuilder/include/EditParameter.h

## Purpose
Header for the `EditParameter` dialog class used in WorldBuilder to edit game parameters.

## Responsibilities
- Provides UI for editing game parameters
- Loads various game data types into combo boxes
- Generates warning/info text for parameters
- Manages parameter editing workflow

## Key Types
- **EditParameter (Class)**: Dialog for editing game parameters
- **SidesList (Class)**: Reference to sides list (forward declared)
- **(anonymous enum) (Enum)**: Dialog resource ID
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### `edit`
- Purpose: Opens the parameter edit dialog
- Calls: Not inferable

### `getWarningText`
- Purpose: Generates warning text for a parameter
- Calls: Not inferable

### `getInfoText`
- Purpose: Generates info text for a parameter
- Calls: Not inferable

### `loadScripts`
- Purpose: Loads scripts into a combo box
- Calls: Not inferable

### `loadWaypoints`
- Purpose: Loads waypoints into a combo box
- Calls: Not inferable

### `loadTransports`
- Purpose: Loads transport units into a combo box
- Calls: Not inferable

### `loadObjectTypeList`
- Purpose: Loads object types into a combo box
- Calls: Not inferable

## Globals
- **m_unitName (AsciiString)**: Stores the unit name for script commands
- **m_sidesListP (SidesList*)**: Pointer to sides list
- **m_selectedLocalizedString (AsciiString)**: Stores selected localized string

## Dependencies
- `GameLogic/Scripts.h`
- `Common/SubsystemInterface.h`
- MFC classes (`CDialog`, `CComboBox
