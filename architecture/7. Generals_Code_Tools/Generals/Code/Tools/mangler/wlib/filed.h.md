# Generals/Code/Tools/mangler/wlib/filed.h

## Purpose
Defines a file output device class for writing text to files.

## Responsibilities
- Inherits from `OutputDevice` to provide file-based output.
- Handles file opening with fallback to "FileDev.out".
- Implements `print` to write strings to the file.
- Manages file resource cleanup in destructor.

## Key Types
- **FileD (Class)**: File output device wrapper for `fprintf`-style writing.

## Key Functions
### FileD::FileD
- Purpose: Constructs a file output device, opening the specified file.
- Calls: `fopen`

### FileD::~FileD
- Purpose: Closes the file handle on destruction.
- Calls: `fclose`

### FileD::print
- Purpose: Writes a string to the file.
- Calls: `new`, `memset`, `memcpy`, `fprintf`, `delete[]`, `fflush`

## Globals
- **out (FILE*)**: The file handle for output.

## Dependencies
- `odevice.h` (base class `OutputDevice`)
- Standard C library functions: `fopen`, `fclose`, `fprintf`, `fflush`, `memset`, `memcpy`
