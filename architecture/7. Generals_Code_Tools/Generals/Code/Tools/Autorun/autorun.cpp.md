# Generals/Code/Tools/Autorun/autorun.cpp

## Purpose
Handles the autorun functionality for Command & Conquer Generals, including CD verification, UI display, and game launch.

## Responsibilities
- Manages the autorun UI window and button interactions
- Verifies CD presence and volume names
- Launches game components (setup, game, uninstall, etc.)
- Handles localization and resource loading
- Manages sound playback and environment validation

## Key Types
- LaunchObjectClass (Class): Handles launching external processes
- MainWindow (Class): Main application window management
- None (Other types not clearly defined in provided context)

## Key Functions
### WinMain
- Purpose: Main program entry point and message loop
- Calls: MainWindow::Register, MainWindow::MainWindow, Main::MessageLoop

### Wnd_Proc
- Purpose: Window procedure for handling messages
- Calls: Dialog_Box_Proc, Stop_Sound_Playing

### Dialog_Box_Proc
- Purpose: Dialog box procedure for handling dialog messages
- Calls: LoadResourceBitmap, CreateDIBPalette, LoadResourceButton

### LaunchObjectClass::Launch
- Purpose: Launches an external process
- Calls: CreateProcess, Cant_Find_MessageBox

### Is_On_CD
- Purpose: Checks if specified volume is present
- Calls: Reformat_Volume_Name

### Prompt_For_CD
- Purpose: Prompts user to insert correct CD
- Calls: CD_Volume_Verification, Show_Message

## Globals
- GlobalMainWindow (MainWindow*): Main application window instance
- Language (int): Current language setting
- LanguageToUse (int): Language to use
- ButtonList (DrawButton*): Array of button objects
- ButtonSizes (RECT): Array of button rectangles
- ButtonImages (char): Array of button image paths
- szVolumeName (char): Current volume name
- OnCDRom (BOOL): Flag indicating if running from CD
- AppMutex (HANDLE): Application mutex handle
- TheFileSystem (FileSystem*): File system interface

## Dependencies
- Windows API headers (windows.h, winuser.h)
- Resource.h, drawbutton.h, autorun.h
- WSYS_FileSystem.h, GameText.h
- Locale_API.h, args.h
- CD control and file system utilities
