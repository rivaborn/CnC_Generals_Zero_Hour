# Generals/Code/Tools/wolSetup/wolSetup.cpp

## Purpose
This file implements the entry point and dialog procedures for the WOL (Westwood Online) setup tool, handling DLL registration and game configuration.

## Responsibilities
- Manages the main application dialog and its message handling
- Handles Generals game setup dialog and configuration
- Registers WOLAPI DLLs (debug/release) via COM registration
- Updates UI display with current WOLAPI and Generals installation status

## Key Types
- None

## Key Functions
### registerDLL
- Purpose: Loads and registers a DLL via its DllRegisterServer export
- Calls: LoadLibrary, GetProcAddress

### GeneralsSetupDialogProc
- Purpose: Handles WM_INITDIALOG and WM_COMMAND for the Generals setup dialog
- Calls: SetDlgItemText, GetDlgItemText, setupGenerals, EndDialog

### updateDisplay
- Purpose: Updates the main dialog's display with current WOLAPI and Generals installation info
- Calls: checkInstalledWolapiVersion, SetDlgItemText

### MainDialogProc
- Purpose: Main message handler for the WOL setup dialog
- Calls: updateDisplay, DialogBox, MessageBox, registerDLL

## Globals
- g_hInst (HINSTANCE): Stores the application instance handle

## Dependencies
- windows.h, stdio.h, stdlib.h
- resource.h, wolSetup.h, verchk.h
- External symbols: LoadLibrary, GetProcAddress, DialogBox, SetDlgItemText, GetDlgItemText, MessageBox, EndDialog
