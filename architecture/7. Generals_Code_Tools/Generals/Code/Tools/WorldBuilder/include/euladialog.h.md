# Generals/Code/Tools/WorldBuilder/include/euladialog.h

## Purpose
Defines the EulaDialog class for displaying an End User License Agreement (EULA) dialog in the WorldBuilder tool.

## Responsibilities
- Inherits from CDialog to create a modal dialog.
- Manages EULA display and user interaction.
- Handles dialog initialization and data exchange.

## Key Types
- EulaDialog (Class): Dialog class for EULA display.
- (anonymous enum) (Enum): Contains IDD_EULA_AGREEMENT identifier.
- IDD (Enum): Dialog resource identifier.

## Key Functions
### EulaDialog()
- Purpose: Standard constructor for EulaDialog.
- Calls: None.

### DoDataExchange()
- Purpose: Handles DDX/DDV data exchange for the dialog.
- Calls: None.

### OnInitDialog()
- Purpose: Initializes the dialog when it is created.
- Calls: None.

### DECLARE_MESSAGE_MAP()
- Purpose: Declares the message map for the dialog class.
- Calls: None.

## Globals
None.

## Dependencies
- CDialog (MFC class)
- CWnd (MFC class)
- CDataExchange (MFC class)
- IDD_EULA_AGREEMENT (resource identifier)
