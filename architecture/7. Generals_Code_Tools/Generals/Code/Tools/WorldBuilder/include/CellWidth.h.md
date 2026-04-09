# Generals/Code/Tools/WorldBuilder/include/CellWidth.h

## Purpose
Header for a modal dialog class that allows users to set the cell width in WorldBuilder.

## Responsibilities
- Define the `CellWidth` dialog class.
- Provide methods to get/set cell width.
- Handle dialog data exchange and user input.

## Key Types
- **CellWidth (Class)**: Modal dialog for setting cell width.
- **(anonymous enum) (Enum)**: Contains `IDD` enum value.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### CellWidth::CellWidth
- Purpose: Constructor for the `CellWidth` dialog.
- Calls: None.

### CellWidth::GetCellWidth
- Purpose: Returns the current cell width value.
- Calls: None.

### CellWidth::DoDataExchange
- Purpose: Handles dialog data exchange (DDX/DDV).
- Calls: None.

### CellWidth::OnOK
- Purpose: Handles OK button click event.
- Calls: None.

### CellWidth::OnInitDialog
- Purpose: Initializes the dialog.
- Calls: None.

### CellWidth::DECLARE_MESSAGE_MAP
- Purpose: Declares the message map for the class.
- Calls: None.

## Globals
- **mCellWidth (int)**: Stores the current cell width value.

## Dependencies
- `CDialog`, `CWnd`, `CDataExchange` (MFC classes).
- `DECLARE_MESSAGE_MAP()` (MFC macro).
