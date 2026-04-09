# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/readline.cpp

## Purpose
Provides functions to read text lines from files or straw objects, handling line endings and trimming whitespace.

## Responsibilities
- Read text lines from `FileClass` or `Straw` objects
- Handle different line endings (CR/LF)
- Trim whitespace from read lines
- Support both char and wchar_t buffers

## Key Types
None

## Key Functions
### Read_Line (FileClass)
- Purpose: Read a line from a file into a char buffer
- Calls: `Read_Line(Straw)`

### Read_Line (Straw, char)
- Purpose: Read a line from a straw object into a char buffer
- Calls: `strtrim`, `strlen`

### Read_Line (Straw, wchar_t)
- Purpose: Read a line from a straw object into a wchar_t buffer
- Calls: `wcstrim`, `wcslen`

## Globals
None

## Dependencies
- `always.h`, `readline.h`, `trim.h`, `wwfile.h`, `xstraw.h`
- `string.h` (for `strlen`, `strtrim`)
- `Straw`, `FileClass` classes
