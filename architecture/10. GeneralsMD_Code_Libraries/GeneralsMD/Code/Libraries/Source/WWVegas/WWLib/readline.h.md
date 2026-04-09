# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/readline.h

## Purpose
Header file declaring functions for reading lines from files or streams.

## Responsibilities
- Declares `Read_Line` functions for different input types.
- Supports both `char` and `wchar_t` buffers.
- Uses `FileClass` and `Straw` for file/stream access.

## Key Types
None

## Key Functions
### Read_Line (FileClass)
- Purpose: Reads a line from a `FileClass` into a `char` buffer.
- Calls: Not inferable (implementation in another file).

### Read_Line (Straw, char)
- Purpose: Reads a line from a `Straw` into a `char` buffer.
- Calls: Not inferable.

### Read_Line (Straw, wchar_t)
- Purpose: Reads a line from a `Straw` into a `wchar_t` buffer.
- Calls: Not inferable.

## Globals
None

## Dependencies
- `straw.h` (for `Straw` class)
- `wwfile.h` (for `FileClass`)
- `<wchar.h>` (for `wchar_t`)
