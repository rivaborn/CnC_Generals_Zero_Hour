# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/CallbackEditor.cpp

## Purpose
Manages a dialog for editing callbacks for user windows in the GUI editor tool.

## Responsibilities
- Provides a dialog procedure for callback editing
- Loads and saves callback strings for windows
- Manages selection of current window being edited
- Handles layout callback initialization/update/shutdown

## Key Types
- None

## Key Functions
### SaveCallbacks
- Purpose: Saves the current callbacks for the selected window
- Calls: `winGetEditData`, `SendDlgItemMessage`

### setCurrentWindow
- Purpose: Sets the active window for editing and updates the dialog
- Calls: `winGetEditData`, `winGetInstanceData`, `SendDlgItemMessage`, `SetWindowText`

### loadUserWindows
- Purpose: Populates a listbox with user windows from the hierarchy
- Calls: `windowIsGadget`, `winGetInstanceData`, `SendMessage`

### saveLayoutCallbacks
- Purpose: Saves layout initialization/update/shutdown callbacks
- Calls: `SendDlgItemMessage`, `TheEditor->setLayoutInit`, `setLayoutUpdate`, `setLayoutShutdown`

### CallbackEditorDialogProc
- Purpose: Main dialog procedure handling messages for the callback editor
- Calls: `InitCallbackCombos`, `loadUserWindows`, `setCurrentWindow`, `SaveCallbacks`, `saveLayoutCallbacks`

## Globals
- `noNameWindowString` (char*): String for unnamed windows
- `currentWindow` (GameWindow*): Tracks the currently edited window

## Dependencies
- `windows.h`, `Common/Debug.h`, `Common/FunctionLexicon.h`, `GameClient/Gadget.h`, `GameClient/GameWindowManager.h`, `GUIEdit.h`, `Resource.h`, `Properties.h`
- Uses `TheEditor`, `TheWindowManager`, `GameWindow`, `GameWindowEditData`, `WinInstanceData`
