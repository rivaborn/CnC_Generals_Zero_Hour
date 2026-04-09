# Generals/Code/Tools/Babylon/ProceedDlg.h

## Purpose
Header file for a dialog class that prompts the user with a message and options to proceed or cancel.

## Responsibilities
- Define the `ProceedDlg` class inheriting from `CDialog`.
- Declare member functions for handling dialog events (Yes, Always, No, Close).
- Manage dialog data exchange and initialization.
- Provide a message display mechanism.

## Key Types
- ProceedDlg (Class): Dialog class for user confirmation prompts.
- (anonymous enum) (Enum): Contains `IDD` enum value for dialog resource ID.
- IDD (Enum): Dialog resource identifier.

## Key Functions
### ProceedDlg/ProceedDlg
- Purpose: Constructor that initializes the dialog with a message.
- Calls: None visible.

### ProceedDlg/DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: None visible.

### ProceedDlg/OnYes
- Purpose: Handles the "Yes" button click event.
- Calls: None visible.

### ProceedDlg/OnAlways
- Purpose: Handles the "Always" button click event.
- Calls: None visible.

### ProceedDlg/OnNo
- Purpose: Handles the "No" button click event.
- Calls: None visible.

### ProceedDlg/OnClose
- Purpose: Handles the dialog close event.
- Calls: None visible.

### ProceedDlg/OnInitDialog
- Purpose: Initializes the dialog when it is created.
- Calls: None visible.

### ProceedDlg/DECLARE_MESSAGE_MAP
- Purpose: Declares the message map for the dialog class.
- Calls: None visible.

## Globals
- IDALWAYS (int): Resource ID for the "Always" button.

## Dependencies
- `CDialog`, `CWnd`, `C
