# Generals/Code/Tools/WorldBuilder/include/BaseBuildProps.h

## Purpose
Defines a dialog class for editing building properties in the WorldBuilder tool.

## Responsibilities
- Manages building property data (name, script, health, unsellable flag)
- Provides UI for editing these properties
- Handles data exchange between UI controls and member variables

## Key Types
- **BaseBuildProps (Class)**: Dialog for editing building properties
- **(anonymous enum) (Enum)**: Contains IDD enum value
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### BaseBuildProps()
- Purpose: Standard constructor for the dialog
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between UI controls and member variables
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog when it's created
- Calls: None

### OnOK()
- Purpose: Handles the OK button click event
- Calls: None

### setProps()
- Purpose: Sets the building property values
- Calls: None

## Globals
- None

## Dependencies
- CDialog (MFC class)
- CDataExchange (MFC class)
- AsciiString (custom string type)
- Int (custom integer type)
- Bool (custom boolean type)
- DECLARE_MESSAGE_MAP() (MFC macro)
