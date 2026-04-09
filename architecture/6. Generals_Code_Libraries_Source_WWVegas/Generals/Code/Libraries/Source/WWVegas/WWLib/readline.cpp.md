# Generals/Code/Libraries/Source/WWVegas/WWLib/readline.cpp

## Purpose
Provides functions to read lines of text from files or straw objects, handling EOF and trimming whitespace.

## Responsibilities
- Read text lines from FileClass or Straw objects
- Handle EOF detection
- Trim leading/trailing whitespace from read lines
- Support both char and wchar_t buffers

## Key Types
None

## Key Functions
### Read_Line (FileClass version)
- Purpose: Read a line from a FileClass object into a char buffer.
- Calls: Read_Line (Straw version)

### Read_Line (Straw char version)
- Purpose: Read a line from a Straw object into a char buffer.
- Calls: strtrim

### Read_Line (Straw wchar_t version)
- Purpose: Read a line from a Straw object into a wchar_t buffer.
- Calls: wcstrim

## Globals
None

## Dependencies
- "always.h", "readline.h", "trim.h", "wwfile.h", "xstraw.h"
- strtrim, wcstrim (from trim.h)
- FileClass, Straw (from wwfile.h, xstraw.h)
