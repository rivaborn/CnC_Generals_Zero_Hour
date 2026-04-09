# Generals/Code/Tools/WorldBuilder/include/NewHeightMap.h

## Purpose
Header file for a dialog class used to configure height map parameters in WorldBuilder.

## Responsibilities
- Define the `TNewHeightInfo` struct for height map configuration
- Declare the `CNewHeightMap` dialog class
- Handle UI interactions for height map settings
- Manage anchor point logic for resizing operations

## Key Types
- **TNewHeightInfo (Struct)**: Stores height map dimensions, initial height, border width, and anchor flags
- **CNewHeightMap (Class)**: Dialog class for configuring height map parameters
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### CNewHeightMap()
- Purpose: Constructor for the height map dialog
- Calls: None

### GetHeightInfo()
- Purpose: Retrieves the current height map configuration
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between UI controls and member variables
- Calls: None

### OnOK()
- Purpose: Handles dialog confirmation
- Calls: None

### OnCommand()
- Purpose: Processes command messages from UI controls
- Calls: None

### doAnchorButton()
- Purpose: Handles anchor button logic for resizing
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog controls
- Calls: None

## Globals
- None

## Dependencies
- `Lib/BaseType.h` (for basic types like Int, Bool)
- MFC classes (`CDialog`, `CDataExchange`, `CWnd`)
- Dialog resource ID `IDD_NewHeightMap`
