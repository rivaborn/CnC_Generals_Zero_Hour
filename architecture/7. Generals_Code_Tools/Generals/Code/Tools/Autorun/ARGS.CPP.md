# Generals/Code/Tools/Autorun/ARGS.CPP

## Purpose
Handles command-line argument parsing for Windows applications.

## Responsibilities
- Parses command-line arguments into an argv-style array
- Handles quoted arguments and whitespace separation
- Provides access to parsed arguments via getter methods
- Manages argument storage and cleanup

## Key Types
- Command_Line_Arguments (Class): Wraps command-line argument parsing functionality
- None: No other significant types defined

## Key Functions
### Command_Line_Arguments::Command_Line_Arguments
- Purpose: Constructor that parses command-line arguments
- Calls: GetModuleFileName, memset

### Command_Line_Arguments::Get_argc
- Purpose: Returns the count of parsed arguments
- Calls: assert

### Command_Line_Arguments::Get_argv
- Purpose: Returns a specific argument by index
- Calls: assert

### Command_Line_Arguments::Set_argv
- Purpose: Sets a specific argument by index
- Calls: assert, strcpy

## Globals
- Args (Command_Line_Arguments*): Global instance of the argument parser

## Dependencies
- windows.h, windowsx.h, assert.h, stdio.h, string.h
- args.h (header file)
- GetCommandLine, GetModuleFileName, memset, assert, strcpy
