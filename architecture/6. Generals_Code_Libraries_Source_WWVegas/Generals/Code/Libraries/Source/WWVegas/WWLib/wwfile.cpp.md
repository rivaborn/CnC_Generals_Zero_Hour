# Generals/Code/Libraries/Source/WWVegas/WWLib/wwfile.cpp

## Purpose
Implements file I/O operations for the FileClass, including formatted printing and indented output.

## Responsibilities
- Provides formatted printing to files via `printf`-style methods
- Handles indented text output for structured logging/debugging
- Manages buffer sizes and variable arguments safely
- Wraps low-level file operations (Write)

## Key Types
- FileClass (Class): Abstract file I/O interface with printf-style methods

## Key Functions
### FileClass::Printf(char *str, ...)
- Purpose: Formats a string into an internal buffer and writes it to the file.
- Calls: `_vsnprintf`, `Write`

### FileClass::Printf(char *buffer, int bufferSize, char *str, ...)
- Purpose: Formats a string into a caller-provided buffer and writes it to the file.
- Calls: `_vsnprintf`, `Write`

### FileClass::Printf_Indented(unsigned depth, char *str, ...)
- Purpose: Formats a string with leading tabs (depth) and writes it to the file.
- Calls: `memset`, `_vsnprintf`, `Write`

## Globals
- None

## Dependencies
- `<stdio.h>`: `_vsnprintf`
- `<stdarg.h>`: `va_list`, `va_start`, `va_end`
- `<memory.h>`: `memset`
- `wwfile.h`: `FileClass`, `PRINTF_BUFFER_SIZE`
