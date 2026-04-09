# Generals/Code/Tools/Launcher/winblows.cpp

## Purpose
Windows-specific launcher code for the Generals game, handling WinMain entry point and command-line parsing.

## Responsibilities
- Parses Windows command-line arguments into argc/argv format
- Initializes global Windows state (instance, command line, show flags)
- Provides utility function for Windows message name lookup
- Calls the main game entry point

## Key Types
- None

## Key Functions
### WinMain
- Purpose: Entry point that initializes globals and parses command line before calling main()
- Calls: GetModuleFileName, main

### Print_WM
- Purpose: Converts Windows message IDs to human-readable strings
- Calls: sprintf

## Globals
- Global_instance (HINSTANCE): Stores the application instance handle
- Global_commandline (LPSTR): Stores the raw command-line string
- Global_commandshow (int): Stores the show window command flag

## Dependencies
- windows.h, windowsx.h, stdlib.h, stdio.h, stdarg.h
- winblows.h (header)
- main (external function)
