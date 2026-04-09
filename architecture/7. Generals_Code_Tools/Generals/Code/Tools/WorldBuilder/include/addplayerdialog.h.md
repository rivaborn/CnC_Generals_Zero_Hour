# Generals/Code/Tools/WorldBuilder/include/addplayerdialog.h

## Purpose
Header for a dialog class used to add players in the WorldBuilder tool.

## Responsibilities
- Manages UI for selecting a player side.
- Stores the selected side internally.
- Provides accessor for the added side.
- Handles dialog initialization and user input.

## Key Types
- **AddPlayerDialog (Class)**: Dialog for adding a player with side selection.
- **(anonymous enum) (Enum)**: Contains IDD constant for dialog resource.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### AddPlayerDialog()
- Purpose: Constructor initializing the dialog with a default side.
- Calls: None.

### getAddedSide()
- Purpose: Returns the selected side as an AsciiString.
- Calls: None.

### DoDataExchange()
- Purpose: Handles data exchange between UI controls and member variables.
- Calls: None.

### OnOK()
- Purpose: Handles OK button click, validates and stores the selected side.
- Calls: None.

### OnCancel()
- Purpose: Handles Cancel button click.
- Calls: None.

### OnInitDialog()
- Purpose: Initializes the dialog UI, populates side selection combo.
- Calls: None.

### OnEditchangeCombo1()
- Purpose: Handles changes in the side selection combo box.
- Calls: None.

## Globals
- None.

## Dependencies
- **GameLogic/SidesList.h**: For side-related logic.
- **CDialog, CWnd, CDataExchange**: MFC dialog classes.
- **AsciiString**: String type used for side names.
