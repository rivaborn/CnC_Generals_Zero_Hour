# Generals/Code/Tools/Babylon/noxstring.cpp

## Purpose
This file implements the main application class for the Babylon tool, handling initialization, Excel integration, and window management.

## Responsibilities
- Manages the MFC application lifecycle
- Checks for running instances of itself and Excel
- Initializes translation databases and paths
- Launches the main dialog

## Key Types
- CNoxstringApp (Class): Main application class
- TransDB (Class): Translation database handler
- None: No custom structs/enums

## Key Functions
### AlreadyRunning
- Purpose: Checks if another instance of the application is running
- Calls: EnumWindows, EnumAllWindowsProcExact

### ExcelRunning
- Purpose: Checks if Microsoft Excel is running
- Calls: EnumWindows, EnumAllWindowsProc

### EnumAllWindowsProc
- Purpose: Callback for enumerating windows to find Excel
- Calls: GetWindowText, strstr

### EnumAllWindowsProcExact
- Purpose: Callback for enumerating windows to find exact title match
- Calls: GetWindowText, strncmp

## Globals
- AppTitle (char[200]): Application title string
- MainDLG (CNoxstringDlg*): Pointer to main dialog
- AppName (char*): Application name prefix
- FoundWindow (HWND): Handle to found window
- theApp (CNoxstringApp): Global application instance
- NoxstrDB (TransDB*): Generals.str database
- MainDB (TransDB*): Main translation database
- NoxstrFilename (char[_MAX_PATH]): Path to Generals.str
- MainXLSFilename (char[_MAX_PATH]): Path to main.db
- DialogPath (char[_MAX_PATH]): Path to dialog files
- RootPath (char[_MAX_PATH]): Root directory path
- CurrentLanguage (LangID): Current language ID
- szSearchTitle (char*): Title to search for in windows

## Dependencies
- stdafx.h, noxstring.h, noxstringDlg.h, xlstuff.h
- MFC classes (CWinApp, COleTemplateServer, etc.)
- Windows API (EnumWindows, GetWindowText, etc.)
- C runtime (sprintf, strcat, etc.)
