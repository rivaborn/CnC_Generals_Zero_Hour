# Generals/Code/Tools/matchbot/wlib/stderrd.h

## Purpose
Defines a stderr output device class for the matchbot tool.

## Responsibilities
- Implements stderr output via `OutputDevice` interface
- Handles string formatting and printing to stderr
- Manages memory allocation/deallocation for output strings

## Key Types
- **StderrD (Class)**: stderr output device implementation

## Key Functions
### StderrD::print
- Purpose: Prints a string to stderr with specified length
- Calls: `new`, `memset`, `memcpy`, `fprintf`, `delete[]`

## Globals
- None

## Dependencies
- `odevice.h` (for `OutputDevice` base class)
- Standard C library functions (`fprintf`, `memset`, `memcpy`)
