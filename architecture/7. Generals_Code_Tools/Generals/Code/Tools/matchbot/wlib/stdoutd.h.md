# Generals/Code/Tools/matchbot/wlib/stdoutd.h

## Purpose
Defines a standard output device class for printing text to stdout.

## Responsibilities
- Inherits from `OutputDevice` to provide stdout-based output.
- Allocates, copies, and prints strings to stdout.
- Ensures output is flushed immediately.
- Manages memory allocation/deallocation for strings.

## Key Types
- **StdoutD (Class)**: Output device that writes to stdout.

## Key Functions
### StdoutD::print
- Purpose: Prints a string to stdout and flushes the buffer.
- Calls: `new[]`, `memcpy`, `fprintf`, `fflush`, `delete[]`.

## Globals
- None.

## Dependencies
- `odevice.h` (for `OutputDevice` base class).
- `fprintf`, `fflush` (C stdio).
- `memcpy`, `new[]`, `delete[]` (C/C++ memory/string ops).
