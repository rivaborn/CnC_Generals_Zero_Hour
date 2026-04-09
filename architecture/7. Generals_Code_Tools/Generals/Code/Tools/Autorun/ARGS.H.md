# Generals/Code/Tools/Autorun/ARGS.H

## Purpose
Defines a class for parsing and managing command-line arguments in the Autorun tool.

## Responsibilities
- Parse command-line arguments from Windows application entry point
- Store and retrieve argument count and values
- Provide access to individual arguments via index

## Key Types
- Command_Line_Arguments (Class): wraps command-line argument parsing and storage
- Args (Global): instance of Command_Line_Arguments for global access

## Key Functions
### Command_Line_Arguments (HINSTANCE, LPTSTR)
- Purpose: Constructor that initializes from Windows application entry parameters
- Calls: Not inferable

### Get_argv (int)
- Purpose: Retrieves a specific command-line argument by index
- Calls: Not inferable

### Get_argc ()
- Purpose: Returns the count of command-line arguments
- Calls: Not inferable

### Set_argv (int, char*)
- Purpose: Sets a specific command-line argument by index
- Calls: Not inferable

## Globals
- Args (Command_Line_Arguments*): global instance for command-line argument access

## Dependencies
- `<windows.h>` for Windows API types (HINSTANCE, LPTSTR)
- Not inferable external symbols
