# Generals/Code/Tools/PATCHGET/WINBLOWS.CPP

## Purpose
Windows-specific entry point and utility functions for the PATCHGET tool.

## Responsibilities
- Provides WinMain as the application entry point
- Parses command-line arguments into argc/argv format
- Converts Windows messages to human-readable strings
- Manages global application state (instance, command line, show state)

## Key Types
None

## Key Functions
### WinMain
- Purpose: Entry point that initializes globals and calls main()
- Calls: GetModuleFileName, main

### Print_WM
- Purpose: Converts Windows message IDs to string representations
- Calls: sprintf

## Globals
- Global_instance (HINSTANCE): Stores the application instance handle
- Global_commandline (LPSTR): Stores the command line string
- Global_commandshow (int): Stores the show state flag

## Dependencies
- Windows.h, Windowsx.h, stdlib.h, stdio.h, stdarg.h
- winblows.h (header)
- GetModuleFileName (Windows API)
- main (external function)
