# Generals/Code/Tools/WW3D/pluglib/bool.h

## Purpose
Defines a `bool` type for C++ compatibility in environments where it's not natively supported.

## Responsibilities
- Provides a portable boolean type definition
- Ensures `true` and `false` constants are available
- Handles compiler-specific cases (MSVC, Borland, Watcom, Unix)

## Key Types
- `bool` (Type): Portable boolean type (unsigned int or enum)
- `false` (Enum): Boolean false constant (0)
- `true` (Enum): Boolean true constant (1)

## Key Functions
None

## Globals
None

## Dependencies
- `"yvals.h"` (MSVC only): For internal compiler definitions
- `TRUE_FALSE_DEFINED`: Guard macro to prevent multiple definitions
- Compiler-specific macros: `_MSC_VER`, `__BORLANDC__`, `__WATCOMC__`, `_UNIX`
