# Generals/Code/Tools/WW3D/max2w3d/logdlg.cpp

## Purpose
Handles a logging dialog for the W3D export tool, providing progress updates and log output during export operations.

## Responsibilities
- Manages a threaded dialog for logging export progress
- Provides formatted output to a rich edit control
- Updates a progress bar during export
- Handles user interaction (OK button) to acknowledge completion
- Initializes and positions the dialog window

## Key Types
- **LogDataDialogClass (Class)**: Main dialog handler for logging and progress updates
- **None**: No other classes/structs/enums defined

## Key Functions
### LogDataDialogClass::printf
- Purpose: Outputs formatted text to the log window
- Calls: `vsprintf`, `SendMessage` (EM_SETSEL, EM_REPLACESEL)

### LogDataDialogClass::rprintf
- Purpose: Replaces the last log entry with new formatted text
- Calls: `vsprintf`, `SendMessage` (EM_SETSEL, EM_REPLACESEL)

### LogDataDialogClass::updatebar
- Purpose: Updates the progress bar based on position/total values
- Calls: `SendMessage` (PBM_SETPOS)

### LogDataDialogClass::Wait_OK
- Purpose: Blocks until user clicks OK to acknowledge log
- Calls: `EnableWindow`, `SetForegroundWindow`

### LogDataDialogClass::Dialog_Proc
- Purpose: Handles Windows messages for the dialog
- Calls: `Dialog_Init`, `EndDialog`

### _logdata_dialog_proc
- Purpose: Thunk function routing messages to LogDataDialogClass
- Calls: `SetProp`, `GetProp`, `RemoveProp`, `LogDataDialogClass::Dialog_Proc`

### _logdata_thread_function
- Purpose: Creates and runs the log dialog in a separate thread
- Calls: `DialogBoxParam`

## Globals
- **None**: No global/static variables

## Dependencies
- Key includes: `logdlg.h`, `resource.h`, `dllmain.h`, `w3dexp.h`, `util.h`, `rawfile.h`, `units.h`
- External symbols: `AppInstance`, Windows API (`CreateThread`, `SendMessage`, `DialogBoxParam`, etc.)
