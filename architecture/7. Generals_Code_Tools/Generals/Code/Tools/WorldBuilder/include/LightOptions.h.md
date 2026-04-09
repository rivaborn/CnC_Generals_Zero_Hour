# Generals/Code/Tools/WorldBuilder/include/LightOptions.h

## Purpose
Header for the LightOptions dialog class used in WorldBuilder to manage light settings for selected map objects.

## Responsibilities
- Define the LightOptions dialog class inheriting from COptionsPanel
- Declare methods for handling UI updates and light selection
- Provide static accessors for the active dialog instance and selected light

## Key Types
- **MapObject (Class)**: Reference to a map object (not defined here)
- **LightOptions (Class)**: Dialog for light editing in WorldBuilder
- **(anonymous enum) (Enum)**: Contains IDD_LIGHT_OPTIONS dialog identifier
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### LightOptions()
- Purpose: Standard constructor for LightOptions dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog when created
- Calls: None

### OnChangeLightEdit()
- Purpose: Handles changes to light edit controls
- Calls: None

### updateTheUI()
- Purpose: Updates the UI to reflect current light settings
- Calls: None

### update()
- Purpose: Static method to update the dialog's UI
- Calls: updateTheUI()

### getSingleSelectedLight()
- Purpose: Returns the currently selected light MapObject
- Calls: None

## Globals
- **m_staticThis (LightOptions*)**: Static reference to the dialog instance
- **m_updating (Bool)**: Flag indicating if UI is updating

## Dependencies
- OptionsPanel.h (base class)
- MFC classes (CWnd, CDataExchange)
- MapObject (forward declared)
