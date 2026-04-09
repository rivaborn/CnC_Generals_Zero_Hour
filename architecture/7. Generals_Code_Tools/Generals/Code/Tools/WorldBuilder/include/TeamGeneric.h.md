# Generals/Code/Tools/WorldBuilder/include/TeamGeneric.h

## Purpose
Defines the `TeamGeneric` class, a property page for team configuration in WorldBuilder.

## Responsibilities
- Manages team properties via a `Dict` object
- Handles dialog initialization and script adjustments
- Populates combo boxes with available scripts
- Synchronizes between UI controls and the underlying dictionary

## Key Types
- **Dict (Class)**: External dictionary for storing team properties
- **TeamGeneric (Class)**: Property page for team configuration
- **(anonymous enum) (Enum)**: Contains `IDD` enum value
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### TeamGeneric()
- Purpose: Standard constructor for the property page
- Calls: None

### setTeamDict()
- Purpose: Sets the team's property dictionary
- Calls: None

### _fillComboBoxesWithScripts()
- Purpose: Populates combo boxes with available scripts
- Calls: Not inferable

### _dictToScripts()
- Purpose: Converts dictionary data to script UI controls
- Calls: Not inferable

### OnInitDialog()
- Purpose: Initializes the dialog and its controls
- Calls: Not inferable

### _scriptsToDict()
- Purpose: Updates the dictionary from script UI controls
- Calls: Not inferable

### OnScriptAdjust()
- Purpose: Handles script adjustment events
- Calls: Not inferable

## Globals
- **m_teamDict (Dict*)**: Stores the team's property dictionary

## Dependencies
- `CPropertyPage` (MFC base class)
- `DECLARE_MESSAGE_MAP()` (MFC macro)
- `afx_msg` (MFC message handler macro)
- `Dict` class (external)
