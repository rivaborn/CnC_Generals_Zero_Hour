# Generals/Code/Tools/PATCHGET/WSTYPES.H

## Purpose
Defines standard type definitions for portability and readability in Westwood Studios projects.

## Responsibilities
- Defines basic integer types (signed/unsigned, 8/16/32-bit)
- Provides boolean constants (TRUE/FALSE)
- Specifies pointer parameter semantics (IN/OUT/INOUT)
- Sets max values for integer types
- Handles platform-specific string comparisons

## Key Types
- `bit8` (typedef): Single-bit flag type
- `sint8`/`uint8` (typedef): 8-bit signed/unsigned integer
- `sint16`/`uint16` (typedef): 16-bit signed/unsigned integer
- `sint32`/`uint32` (typedef): 32-bit signed/unsigned integer

## Key Functions
None

## Globals
- `TRUE` (macro): Boolean true value (1)
- `FALSE` (macro): Boolean false value (0)
- `IN`/`OUT`/`INOUT` (macro): Pointer parameter semantics markers
- `MAX_*` (macro): Maximum values for each integer type

## Dependencies
- Platform-specific macros (`_WIN32`, `_strnicmp`, `_stricmp`)
