# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwhack.h

## Purpose
Defines a macro for forcing module linkage in a library to ensure inclusion in the executable.

## Responsibilities
- Provides `FORCE_LINK` macro to enforce module linking
- Declares corresponding `_Force_Link_` function template
- Prevents duplicate inclusion via header guards

## Key Types
None

## Key Functions
### `DECLARE_FORCE_LINK(module)`
- Purpose: Declares the linker function for the `FORCE_LINK` macro.
- Calls: None

## Globals
None

## Dependencies
- Uses `_MSC_VER` for Microsoft compiler version check
- Relies on standard C++ preprocessor directives (`#ifdef`, `#define`, etc.)
