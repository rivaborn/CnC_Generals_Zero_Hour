# Generals/Code/Tools/Launcher/filed.h

## Purpose
Defines a file-based output device for logging or debugging.

## Responsibilities
- Opens a file for writing output
- Writes strings to the file
- Optionally outputs to debug console
- Manages file handle lifecycle

## Key Types
- **FileD (Class)**: File-based output device that extends OutputDevice

## Key Functions
### FileD::FileD
- Purpose: Constructor that opens the specified file for writing
- Calls: `fopen`

### FileD::~FileD
- Purpose: Destructor that closes the file handle
- Calls: `fclose`

### FileD::print
- Purpose: Writes a string to the file and optionally to debug output
- Calls: `new`, `memset`, `memcpy`, `fprintf`, `OutputDebugString`, `delete[]`, `fflush`

## Globals
- **out (FILE*)**: File handle for output
- **m_outputDebug (bool)**: Flag to enable debug console output

## Dependencies
- `odevice.h` (OutputDevice base class)
- `fopen`, `fclose`, `fprintf`, `fflush` (C stdio)
- `OutputDebugString` (Windows API)
