# Generals/Code/Tools/matchbot/wlib/filed.h

## Purpose
Defines a file output device class for writing text to files.

## Responsibilities
- Opens a file for writing (or falls back to "FileDev.out")
- Provides a print method to write strings to the file
- Manages file resource cleanup via destructor

## Key Types
- FileD (Class): Output device that writes to a file

## Key Functions
### FileD::FileD
- Purpose: Constructor that opens the specified file.
- Calls: fopen

### FileD::~FileD
- Purpose: Destructor that closes the file.
- Calls: fclose

### FileD::print
- Purpose: Writes a string to the file.
- Calls: new, memset, memcpy, fprintf, delete[], fflush

## Globals
- None

## Dependencies
- "odevice.h" (OutputDevice base class)
- FILE (from stdio.h)
- fopen, fclose, fprintf, fflush, memset, memcpy (from stdio.h and string.h)
