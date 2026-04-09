# Generals/Code/Tools/WW3D/max2w3d/exportlog.h

## Purpose
Defines the ExportLog class for managing export progress logging during 3D model conversion.

## Responsibilities
- Provides static methods for initializing/shutting down the export log dialog
- Offers formatted output (printf/rprintf) for logging
- Supports progress bar updates via updatebar

## Key Types
- ExportLog (Class): Interface for export progress logging and UI updates

## Key Functions
### Init
- Purpose: Initializes the export log dialog with a parent window
- Calls: None

### Shutdown
- Purpose: Closes the export log dialog and optionally waits for user acknowledgment
- Calls: None

### printf
- Purpose: Logs formatted text to the export dialog
- Calls: None

### rprintf
- Purpose: Logs formatted text with a newline to the export dialog
- Calls: None

### updatebar
- Purpose: Updates the progress bar position in the export dialog
- Calls: None

## Globals
- None

## Dependencies
- `<windows.h>` for HWND type
- No external symbols used
