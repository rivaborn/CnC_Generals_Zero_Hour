# Generals/Code/Tools/WW3D/max2w3d/logdlg.h

## Purpose
Defines a logging dialog class for the max2w3d tool, providing a UI for displaying log messages and progress.

## Responsibilities
- Manages a modal dialog for logging output
- Provides formatted logging methods (printf/rprintf)
- Handles progress bar updates
- Waits for user acknowledgment (OK button)

## Key Types
- LogDataDialogClass (Class): Manages the logging dialog window and its functionality

## Key Functions
### LogDataDialogClass::Wait_OK
- Purpose: Blocks until the user clicks OK
- Calls: Not inferable

### LogDataDialogClass::printf
- Purpose: Formats and displays a log message
- Calls: Not inferable

### LogDataDialogClass::rprintf
- Purpose: Formats and displays a log message (reentrant version)
- Calls: Not inferable

### LogDataDialogClass::updatebar
- Purpose: Updates the progress bar position
- Calls: Not inferable

### LogDataDialogClass::Dialog_Proc
- Purpose: Handles Windows messages for the dialog
- Calls: Not inferable

### LogDataDialogClass::Dialog_Init
- Purpose: Initializes the dialog controls
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<windows.h>` for Windows API types
- External symbols: `HWND`, `WPARAM`, `LPARAM`, `HANDLE`, `DWORD`, `va_list`
