# Generals/Code/Tools/mangler/wlib/stdoutd.h

## Purpose
Defines a standard output device class for printing to stdout.

## Responsibilities
- Implements an output device that writes to standard output.
- Handles memory allocation and deallocation for output strings.
- Ensures output is flushed immediately.

## Key Types
- **StdoutD (Class)**: Output device that prints to stdout.

## Key Functions
### StdoutD::print
- Purpose: Prints a string to stdout and flushes the buffer.
- Calls: `new`, `memcpy`, `fprintf`, `fflush`, `delete[]`.

## Globals
- None.

## Dependencies
- `odevice.h` (inherits from `OutputDevice`).
- Standard C library functions: `fprintf`, `fflush`, `memcpy`.
