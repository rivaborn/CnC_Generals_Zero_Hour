# Generals/Code/Libraries/Source/WWVegas/WWLib/readline.h

## Purpose
Header file declaring functions for reading lines from files or streams.

## Responsibilities
- Declares line-reading functions for different input types
- Provides overloads for char and wchar_t buffers
- Uses FileClass and Straw for file/stream access

## Key Types
None

## Key Functions
### Read_Line
- Purpose: Reads a line from a FileClass into a char buffer
- Calls: Not inferable

### Read_Line
- Purpose: Reads a line from a Straw into a char buffer
- Calls: Not inferable

### Read_Line
- Purpose: Reads a line from a Straw into a wchar_t buffer
- Calls: Not inferable

## Globals
None

## Dependencies
- "straw.h" (Straw class)
- "wwfile.h" (FileClass)
- <wchar.h> (wchar_t)
