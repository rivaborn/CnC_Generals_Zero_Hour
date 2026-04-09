# Generals/Code/Tools/mangler/wlib/wstypes.h

## Purpose
Defines standard type aliases and macros for portability and readability in the Westwood Studios toolchain.

## Responsibilities
- Provides fixed-width integer and floating-point type aliases
- Defines common macros (TRUE, FALSE, MIN, MAX, NULL)
- Ensures thread-safe behavior on reentrant builds
- Standardizes input/output parameter annotations (IN, OUT, INOUT)
- Platform-specific adjustments (Windows vs. POSIX)

## Key Types
- bit8 (typedef): 8-bit signed integer
- sint8 (typedef): 8-bit signed integer
- uint8 (typedef): 8-bit unsigned integer
- sint16 (typedef): 16-bit signed integer
- uint16 (typedef): 16-bit unsigned integer
- sint32 (typedef): 32-bit signed integer
- uint32 (typedef): 32-bit unsigned integer
- float32 (typedef): 32-bit floating-point
- float64 (typedef): 64-bit floating-point

## Key Functions
None

## Globals
None

## Dependencies
- `<time.h>`, `<stdlib.h>`, `<stdio.h>`, `<string.h>`
- `<unistd.h>`, `<sys/time.h>`, `<dirent.h>` (POSIX)
- `<time.h>`, `<sys/timeb.h>` (Windows)
- `"threadsafe.h"` (custom header)
