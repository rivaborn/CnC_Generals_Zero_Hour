# Generals/Code/Tools/WW3D/max2w3d/exportlog.cpp

## Purpose
Manages export logging functionality for the Max2W3d tool, providing a logging system with progress tracking.

## Responsibilities
- Initialize and shutdown the logging dialog
- Output formatted log messages to the UI
- Update progress bar in the log window
- Handle variable argument formatting for log output

## Key Types
- None

## Key Functions
### ExportLog::Init
- Purpose: Creates and initializes the log dialog window
- Calls: `new LogDataDialogClass`

### ExportLog::Shutdown
- Purpose: Cleans up the log dialog, optionally waiting for user acknowledgment
- Calls: `_LogDialog->Wait_OK()`, `delete _LogDialog`

### ExportLog::printf
- Purpose: Formats and outputs a log message to the dialog
- Calls: `va_start`, `_LogDialog->printf`

### ExportLog::rprintf
- Purpose: Overwrites the last log line with new content
- Calls: `va_start`, `_LogDialog->rprintf`

### ExportLog::updatebar
- Purpose: Updates the progress bar position in the log window
- Calls: `_LogDialog->updatebar`

## Globals
- `_LogDialog` (LogDataDialogClass*): Stores the instance of the log dialog

## Dependencies
- `exportlog.h`, `logdlg.h`, `<assert.h>`
- `LogDataDialogClass`, `HWND`, `va_list`
