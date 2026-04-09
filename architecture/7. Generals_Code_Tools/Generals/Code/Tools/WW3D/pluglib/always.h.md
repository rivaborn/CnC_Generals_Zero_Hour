# Generals/Code/Tools/WW3D/pluglib/always.h

## Purpose
Provides compiler-specific defines, macros, and utility functions for cross-platform compatibility in the SAGE engine.

## Responsibilities
- Defines `min`/`max` macros and template functions to avoid conflicts with system headers
- Configures compiler-specific settings (warnings, inlining, memory debugging)
- Provides utility macros like `ARRAY_SIZE` and `size_of`
- Disables conflicting system macros (e.g., `NOMINMAX`)

## Key Types
- None

## Key Functions
### `min<T>(T a, T b)`
- Purpose: Returns the smaller of two values.
- Calls: None

### `max<T>(T a, T b)`
- Purpose: Returns the larger of two values.
- Calls: None

## Globals
- `NULL` (macro): Defined as `0` if not already defined
- `ARRAY_SIZE` (macro): Computes the number of elements in an array
- `size_of` (macro): Computes the size of a struct member

## Dependencies
- Compiler-specific headers (`borlandc.h`, `visualc.h`, `watcom.h`)
- STL headers (`<crtdbg.h>`, `<stdlib.h>`, `<malloc.h>`) for debug builds
- Uses `_MSC_VER`, `__ICL`, `__BORLANDC__`, `__WATCOMC__` for compiler detection
